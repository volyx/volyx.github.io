---
author: "volyx"
title:  "Maven Dependencies"
date: "2015-01-12"
# description: "Sample article showcasing basic Markdown syntax and formatting for HTML elements."
tags:  ["old-posts"]
categories: ["old-posts"]
summary: "123"
image: "../img/netty.jpg"
# series: ["Themes Guide"]
# aliases: ["migrate-from-jekyl"]
# ShowToc: true
# TocOpen: true
# weight: 2
---

image::../../img/learning_openshift.jpg[]

Анализировать зависимости в вашем мавен проекте можно с помощью команды `dependency:analyze`.

Analyze your Maven Project Dependencies with dependency:analyze
When working on a larger Maven project it might happen that you lose track of the dependecies in your project. Over time you are adding new dependencies, remove code or move code to modules so some of the dependencies become obsolete. Though I did lots of Maven projects I have to admit I didn't know until recently that the dependency plugin contains a useful goal for solving this problem: dependency:analyze.

The dependency:analyze mojo can find dependencies that are declared for your project but are not necessary. Additionally it can find dependecies that are used but are undeclared, which happens when you are directly using transitive dependencies in your code.

Analyzing Dependencies
I am showing an example with the Odftoolkit project. It contains quite some dependencies and is old enough that some of them are outdated. ODFDOM is the most important module of the project, providing low level access to the Open Document structure from Java code. Running mvn dependency:tree we can see its dependencies at the time of writing:

[source]
----
mvn dependency:tree
[INFO] Scanning for projects...
[INFO]                                                                         
[INFO] ------------------------------------------------------------------------
[INFO] Building ODFDOM 0.8.10-incubating-SNAPSHOT
[INFO] ------------------------------------------------------------------------
[INFO] 
[INFO] --- maven-dependency-plugin:2.1:tree (default-cli) @ odfdom-java ---
[INFO] org.apache.odftoolkit:odfdom-java:jar:0.8.10-incubating-SNAPSHOT
[INFO] +- org.apache.odftoolkit:taglets:jar:0.8.10-incubating-SNAPSHOT:compile
[INFO] |  \- com.sun:tools:jar:1.7.0:system
[INFO] +- xerces:xercesImpl:jar:2.9.1:compile
[INFO] |  \- xml-apis:xml-apis:jar:1.3.04:compile
[INFO] +- junit:junit:jar:4.8.1:test
[INFO] +- org.apache.jena:jena-arq:jar:2.9.4:compile
[INFO] |  +- org.apache.jena:jena-core:jar:2.7.4:compile
[INFO] |  +- commons-codec:commons-codec:jar:1.5:compile
[INFO] |  +- org.apache.httpcomponents:httpclient:jar:4.1.2:compile
[INFO] |  +- org.slf4j:jcl-over-slf4j:jar:1.6.4:compile
[INFO] |  +- org.apache.httpcomponents:httpcore:jar:4.1.3:compile
[INFO] |  +- org.slf4j:slf4j-api:jar:1.6.4:compile
[INFO] |  +- org.slf4j:slf4j-log4j12:jar:1.6.4:compile
[INFO] |  \- log4j:log4j:jar:1.2.16:compile
[INFO] +- org.apache.jena:jena-core:jar:tests:2.7.4:test
[INFO] +- net.rootdev:java-rdfa:jar:0.4.2:compile
[INFO] |  \- org.apache.jena:jena-iri:jar:0.9.1:compile
[INFO] \- commons-validator:commons-validator:jar:1.4.0:compile
[INFO]    +- commons-beanutils:commons-beanutils:jar:1.8.3:compile
[INFO]    +- commons-digester:commons-digester:jar:1.8:compile
[INFO]    \- commons-logging:commons-logging:jar:1.1.1:compile
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time: 1.877s
[INFO] Finished at: Mon Jan 20 00:41:05 CET 2014
[INFO] Final Memory: 13M/172M
[INFO] ------------------------------------------------------------------------
The project contains some direct dependencies with a lot of transitive dependencies. When running mvn dependency:analyze on the project we will see that our dependencies don't seem to be correct:

mvn dependency:analyze
[INFO] Scanning for projects...
[INFO]                                                                         
[INFO] ------------------------------------------------------------------------
[INFO] Building ODFDOM 0.8.10-incubating-SNAPSHOT
[INFO] ------------------------------------------------------------------------
[INFO] 
[...] 
[INFO] <<< maven-dependency-plugin:2.1:analyze (default-cli) @ odfdom-java <<<
[INFO] 
[INFO] --- maven-dependency-plugin:2.1:analyze (default-cli) @ odfdom-java ---
[WARNING] Used undeclared dependencies found:
[WARNING]    org.apache.jena:jena-core:jar:2.7.4:compile
[WARNING]    xml-apis:xml-apis:jar:1.3.04:compile
[WARNING] Unused declared dependencies found:
[WARNING]    org.apache.odftoolkit:taglets:jar:0.8.10-incubating-SNAPSHOT:compile
[WARNING]    org.apache.jena:jena-arq:jar:2.9.4:compile
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time: 4.769s
[INFO] Finished at: Mon Jan 20 00:43:27 CET 2014
[INFO] Final Memory: 28M/295M
[INFO] ------------------------------------------------------------------------
----

The second part of the warnings is easier to understand; we have declared some dependencies that we are never using, the taglets and jena-arq. When comparing this with the output we got above you will notice that the largest set of transitive dependencies was imported by the jena-arq dependency. And we don't even need it.

The first part seems to be more difficult: there are two used but undeclared dependencies found. What does it mean? Shouldn't compiling fail if there are any dependencies that are undeclared? No, it just means that we are directly using a transitive dependency from our code which we should better declare ourselves.

Breaking the Build on Dependency Problems
If you want to find problems with your dependencies as early as possible it's best to integrate the check in your build. The dependency:analyze goal we have seen above is meant to be used in a standalone way, for automatic execution there is the analyze-only mojo. It automatically binds to the verify phase and can be declared like this:

<plugin>
    <artifactId>maven-dependency-plugin</artifactId>
    <version>2.8</version>
    <executions>
        <execution>
            <id>analyze</id>
            <goals>
                <goal>analyze-only</goal>
            </goals>
            <configuration>
                <failOnWarning>true</failOnWarning>
                <outputXML>true</outputXML>
            </configuration>
        </execution>
    </executions>
</plugin>
Now the build will fail if there are any problems found. Conveniently, if an undeclared dependency has been found, it will also output the XML that you can then paste in your pom file.

A final word of caution: the default analyzer works on the bytecode level so in special cases it might not notice a dependency correctly, e.g. when you are using constants from a dependency that are inlined.