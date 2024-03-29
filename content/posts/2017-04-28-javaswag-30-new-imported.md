---
author: "volyx"
title:  "Javaswag выпуск 30"
date: "2017-04-28"
# description: "Sample article showcasing basic Markdown syntax and formatting for HTML elements."
tags:  ["old-posts"]
categories: ["old-posts"]
summary: "В выпуске загружаем CPU по полной используя ForkJoinPool, строим архитектуру минимальными средствами и разбираемся что будет с Reflection в Java 9."
image: ""
# series: ["Themes Guide"]
# aliases: ["migrate-from-jekyl"]
# ShowToc: true
# TocOpen: true
# weight: 2
---

Привет!
В выпуске загружаем CPU по полной используя ForkJoinPool, строим архитектуру минимальными средствами и разбираемся что будет с Reflection в Java 9.

[http://blog.sokolenko.me/2014/11/javavm-options-production.html](http://blog.sokolenko.me/2014/11/javavm-options-production.html)

**Java VM Options You Should Always Use in Production**

Каждый раз гуглю эту статью, когда не могу вспомнить, как настроить ротацию логов для сборщика мусора. Решил увековечить ее за это в рассылке. Она мне помогла уже не один раз.

[https://www.sitepoint.com/reflection-vs-encapsulation-in-the-java-module-system/](https://www.sitepoint.com/reflection-vs-encapsulation-in-the-java-module-system/)

**Reflection vs Encapsulation – Stand Off in the Java Module System**

Николай Парлог рассказывает что будет с рефлекшенем в джаве 9. Если вкратце, то мы сможем управлять видимостью объектов через рефлекшен с помощью "директив" в module-info.java 

[https://youtu.be/rUDGQQ83ZtI](https://youtu.be/rUDGQQ83ZtI)

**Turbo Charge CPU Utilization in Fork/Join Using the ManagedBlocker by Heinz Kabutz**

Хайнз рассказывает как заставить процессор работать на все 100%. Разгоняет он его используя ForkJoinPool и RecursiveTask. Не обошлось без написания своего метода умножения для BigInteger.

[https://www.infoq.com/presentations/java-9-gc](https://www.infoq.com/presentations/java-9-gc)

**Goodbye PrintGCDetails... and Other JDK 9 Changes!**

От том как изменится вывод сборщика мусора в джаве 9.

[https://dzone.com/articles/the-garage-architecture](https://dzone.com/articles/the-garage-architecture)

**The Garage Architecture**

Учимся строить архитектуру из **вна и палок. Как бы выглядела архитектура приложения-стартапа из гаража.

[https://balamaci.ro/kafka-streams-for-stream-processing/](https://balamaci.ro/kafka-streams-for-stream-processing/)

**Kafka Streams for Stream processing**

**A few words about how Kafka works.**

Статью стоило назвать  "Кафка квик старт для джава разработчика". В статье рассказывается, что такое Кафка, с примерами, как запустить ее на своем компьютере с несколькими “консюмерами” и “продюсерами”

[https://tanyg.in/ia-tvoi-ghipiervizor-v-ighrie-sinii-kit-ili-docker-v-tiestirovanii/](https://tanyg.in/ia-tvoi-ghipiervizor-v-ighrie-sinii-kit-ili-docker-v-tiestirovanii/)

**Я твой гипервизор в игре "Синий кит", или Docker в тестировании
**Автор рассказывает о преимуществах запуска тестов в докере. Запускает селениум тесты в контейнере и делится проблемами.

**[http://cr.openjdk.java.net/~briangoetz/amber/pattern-match.htm**l](http://cr.openjdk.java.net/~briangoetz/amber/pattern-match.html)

**Pattern Matching for Java**

На странице всем известного Брайна Гетца выложена статья о том, как мог бы выглядеть паттерн матчинг в джаве. Написано, что ни в коем случае не обещают паттерн матчинг ни в каких ближайших релизах, но вопрос - зачем тогда писать статью об этом? Наверняка, архитекторы джавы втихаря подумывают об этом.

[https://github.com/testcontainers/testcontainers-java](https://github.com/testcontainers/testcontainers-java)

**TestContainers
**Не могу не поделиться классной библиотекой для запуска докер контейнеров для ваших интеграционных тестов. Хватит писать моки на базу данных, поднимите настояющую!
