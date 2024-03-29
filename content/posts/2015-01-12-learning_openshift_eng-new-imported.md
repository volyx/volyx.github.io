---
author: "volyx"
title:  "Reviewing book Learning OpenShift"
date: "2015-01-12"
# description: "Sample article showcasing basic Markdown syntax and formatting for HTML elements."
tags:  ["old-posts"]
categories: ["old-posts"]
summary: ""
image: ""
# series: ["Themes Guide"]
# aliases: ["migrate-from-jekyl"]
# ShowToc: true
# TocOpen: true
# weight: 2
---

image::../../img/learning_openshift.jpg[]

https://www.openshift.com/[Openshift] was attractive for me in early days their beginnings. I'm really now don't remember when my first application was deployed. Over the years I was seeing many other PaaS, but every time when I was touching their, and when unexpectedly I was needing to quick deploying of my java application - I was returning back after some time. As for me, i think, it's most comfortable service for quick deployment and prototyping your applications.

Over this years he is growing up and start supporting many frameworks and technologies . Naturally, I'm was especially interested in such projects as apache tomcat, jboss eap, mysql, mongodb. Full list of supported technologies you can see in https://marketplace.openshift.com/home[openshift market] 

When i was getting offer to write small review on book https://www.packtpub.com/virtualization-and-cloud/learning-openshift[Learning Openshift] I don't thinking a lot and quickly agree, because it was curious for me: "Could be that I skipped something very important for me about openshift?".

Since I consider myself a very experienced user https://www.openshift.com/[openshift], bronze plan, after all. I briefly ran the first chapter, because all of these steps to configure many times I cranked on different machines, their home and knew almost by heart. My attention was drawn to Chapter 6, which shows an example of the rapid development of java-application using spring, mongodb. An example of how quickly write such an application and I would like to bring here. Materials taken from books. 

For the impatient http://mlbparks-onpaas.rhcloud.com/ here's an example of what happens in the end application. If a site does not start immediately - refresh a few times, it happens. 

And of course the shortest and most guide how to make a similar application and picture to be interested.

image::../../img/learning_openshift_1.jpg[]

[source,bash]
----
$ rhc app create springmlb tomcat7 mongodb-2.4 --from-code https://github.com/gshipley/springmlb.git
----

This is for those who have already registered and established in openshift `rhc`, ask for others to follow here https://developers.openshift.com/en/overview-what-is-openshift.html. This is not difficult.

After the command to connect to our application using `ssh` for this in the console run the command.

[source,bash]
----
$ rhc app ssh springmlb
----
https://developers.openshift.com/en/managing-remote-connection.html[Документация по ключам ssh]

After we connect to our car load json data file and save it in a folder `/ tmp` on the remote machine. To do this, run the command:

[source,bash]
----
$ cd /tmp
$ wget https://raw.github.com/gshipley/springmlb/master/mlbparks.json
----
Import everything in Mongo
[source,bash]
----
$ mongoimport --jsonArray -d $OPENSHIFT_APP_NAME -c teams --type json --file /tmp/mlbparks.json  -h $OPENSHIFT_MONGODB_DB_HOST --port $OPENSHIFT_MONGODB_DB_PORT -u $OPENSHIFT_MONGODB_DB_USERNAME  -p $OPENSHIFT_MONGODB_DB_PASSWORD
----
Then you can check by going to the appropriate `url`

image::../../img/learning_openshift_2.jpg[]

Just a very good example of the development of similar applications is here https://blog.openshift.com/day-22-developing-single-page-applications-with-spring-mongodb-and-angularjs/[developing-single-page-applications-with-spring-mongodb-and-angularjs]
This blog author https://github.com/shekhargulati[Shekhar Gulati], he has a very interesting https://blog.openshift.com/learning-30-technologies-in-30-days-a-developer-challenge/ [series of articles] in which it within 30 days of developing one application per day, using openshift.

