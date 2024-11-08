---
author: "volyx"
title:  "Javaswag выпуск 19"
date: "2016-10-26"
# description: "Sample article showcasing basic Markdown syntax and formatting for HTML elements."
tags:  ["old-posts"]
categories: ["old-posts"]
summary: "В выпуске тонкости экзекъютор сервисов, сохранение объектов в Редис и способы упаковки приложения в исполняемый архив."
image: ""
# series: ["Themes Guide"]
# aliases: ["migrate-from-jekyl"]
# ShowToc: true
# TocOpen: true
# weight: 2
---
Привет!
В выпуске тонкости экзекъютор сервисов, сохранение объектов в Редис и способы упаковки приложения в исполняемый архив.

[PostConstruct and constructor injection](https://www.knitelius.com/2016/10/05/understanding-dependency-injection-part-2-postconstruct-and-constructor-injection/)

Если вы не помните в какой последовательности вызывается @Inject и @PostConstruct — эта статья для вас. На примерах кода автор показывает какие механизмы скрыты за этими аннотациями внутри IoC контейнера.

[Small scale stream processing kata. Part 1: thread pools](http://www.nurkiewicz.com/2016/10/small-scale-stream-processing-kata-part.html)

Автор блога описывает построение архитектуры приложения, которое должно обрабатывать данные в реальном времени со скоростью 1000 запросов в секунду. 


[Securing JAX-RS Endpoints with JWT](https://antoniogoncalves.org/2016/10/03/securing-jax-rs-endpoints-with-jwt/)

В статье рассказывается как защитить REST сервисы с помощью JWT токенов. 
Вы узнаете как написать несколько своих аннотаций и фильтров чтобы самому реализовать систему защиты АПИ приложения.


[A Look at the Java Distributed In-Memory Data Model (Powered by Redis)](https://dzone.com/articles/java-distributed-in-memory-data-model-powered-by-r)

Библиотека Redison превращает джава объекты в так называемые “живые объекты”. Те в свою очередь, делегируют любые вызовы методов вызовам к Редису. Таким образом живые объекты всегда сохраняют свое состояние в Редис и всегда актуальны. 


[Java Bytecode 101](https://speakerdeck.com/antonarhipov/java-bytecode-101)

Презентация Антона Архипова с питерской конференции Джокер. Для всех, кто хочет разобраться как работает виртуальная машина Джава или написать свой интерпретатор байткода. 


[Android Networking Tutorial: Getting Started](https://www.raywenderlich.com/126770/android-networking-tutorial-getting-started)

В статье создается Андройд-приложение, которое отображает репозитории с Гитхаба. Акцент делается на работу с сетью.  Хорошая статья перед стартом вашего первого приложения на Андроид.


[Retrying operation with Guava Retrying](http://www.ashishpaliwal.com/blog/2015/03/java-tip-retrying-operation-with-guava-retrying/)

Guava Retrying - библиотека позволяет оборачивать методы в “ретрай обертку”, которая реализует повтор операции за вас. Парсили вы сайт и оборвался интернет — библиотека позволяет настроить количество повторов, таймауты, период через который нужно повторить операцию и много чего еще. 


[Mother F**k the ScheduledExecutorService!](http://code.nomad-labs.com/2011/12/09/mother-fk-the-scheduledexecutorservice/)

Я столкнулся с этим буквально на этой неделе. Вы знали что ScheduledThreadPoolExecutor не бросает Рантайм ошибки? Если в коде где-то спрятался NullPointerException экзекъютор не показывает ошибку, а продолжает спокойно выполняться — будьте осторожней с ним и прочитайте обязательно статью. 

[How to get the running tasks for a Java Executor](https://www.richardnichols.net/2012/01/how-to-get-the-running-tasks-for-a-java-executor/)

В статье рассказывается как написать свой экзекъютор для того чтобы мониторить текущие потоки — какие выполняются, а какие уже выполнились.

[A Simple Multi-Threaded Java HTTP Proxy Server](http://www.jtmelton.com/2007/11/27/a-simple-multi-threaded-java-http-proxy-server/)

Если вы когда-нибудь задумывались как реализованы прокси-сервера, то вам понравится эта статья. Автор написал свою реализацию прокси сервера на джаве. Она конечно, не готова к использованию в продакшене — но точно поможет разобраться как все устроено.

[How to Create an Executable JAR with Maven](http://www.baeldung.com/executable-jar-with-maven)

В статье 6 способов как можно с помощью мавен плагинов сделать запускаемый jar-файл.

Еженедельные выпуски Джавасвэга на почту — [http://javaswag.curated.co](http://javaswag.curated.co).

Еженедельные выпуски Джавасвэга в Телеграме — [http://telegram.me/javaswag](http://telegram.me/javaswag).

Удачи!
