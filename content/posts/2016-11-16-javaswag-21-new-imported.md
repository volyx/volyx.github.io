---
author: "volyx"
title:  "Javaswag выпуск 21"
date: "2016-11-16"
# description: "Sample article showcasing basic Markdown syntax and formatting for HTML elements."
tags:  ["old-posts"]
categories: ["old-posts"]
summary: "В выпуске gRPC, нативная компиляция Java кода и показ метрик из Спринг приложения."
image: ""
# series: ["Themes Guide"]
# aliases: ["migrate-from-jekyl"]
# ShowToc: true
# TocOpen: true
# weight: 2
---
В выпуске gRPC, нативная компиляция Java кода и показ метрик из Спринг приложения.

[Enabling Googley microservices with HTTP/2 and gRPC](http://www.slideshare.net/borisovalex/enabling-googley-microservices-with-http2-and-grpc)

Если в вашем проекте понадобился RPC(Remote Procedure Call), то обязательно посмотрите на gRPC. gRPC – популярный фреймворк от Гугла поверх протокола HTTP/2. По ссылке слайды из доклада Алекса Борисова с примерами использования и основными концепциями . 


[Flame graphs and perf-top for JVMs inside Docker containers](http://batey.info/docker-jvm-flamegraphs.html)

Флейм графы — новый способ отображения количества использованного CPU приложением. Автор статьи рассказывает как можно написать несколько скриптов для построения флейм графов Java приложения, запущенного в докере.

[Introduction to FindBugs](http://www.baeldung.com/intro-to-findbugs)

FindBugs — статический анализатор для Java кода. Анализатор просматривает код и выдает список потенциальных ошибок. В статье рассказывается как запускать FindBugs из IDE и встраивать его в процесс сборки приложения.


[Introduction to WebJars](http://www.baeldung.com/maven-webjars)

В статье рассказывается  как с помощью мавена можно встроить css и javascript библиотеки в ваше приложение. На примере спринг приложения автор рассказывает как с помощью нескольких строк кода добавить в проект Jquery и bootstrap.


[Native Ahead-of-Time Compilation in Java](https://www.voxxed.com/blog/2016/10/native-ahead-time-compilation-java/)

В Java 9 появится возможность компилировать приложение в нативный код. В статье краткое описание утилиты `jaotc` и видео c JVM Language Summit


[Groovy Excel Builder](http://jameskleeh.com/groovy-excel-builder)

Библиотека Groovy Excel Builder предлагает удобный DSL для создания Excel файлов. Apache POI используется внутри, а снаружи используется лаконичный АПИ — все то за что так любят Groovy.


[Exposing JVM metrics in Spring Boot applications using Dropwizard metric library](http://www.heapwhisperer.com/2015/07/exposing-jvm-metrics-in-spring-boot.html)

Как вы собираете метрики из своего приложения? В статье рассказывается о том, как встроить библиотеку Metrics в Спринг приложение чтобы собирать всю необходимую статистику.

Еженедельные выпуски Джавасвэга на почту — [http://javaswag.curated.co](http://javaswag.curated.co).

Еженедельные выпуски Джавасвэга в Телеграме — [http://telegram.me/javaswag](http://telegram.me/javaswag).

Удачи!

![dilbert21](/images/dilbert21.jpeg)