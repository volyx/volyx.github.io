---
author: "volyx"
title:  "Javaswag выпуск 31"
date: "2017-05-18"
# description: "Sample article showcasing basic Markdown syntax and formatting for HTML elements."
tags:  ["old-posts"]
categories: ["old-posts"]
summary: "В выпуске декомпозируем микросервисы с помощью RabbitMq, читаем мнение о Jigsaw от разработчика ByteBuddy и узнаем, что думает главный архитектор джавы насчет этого."
image: ""
# series: ["Themes Guide"]
# aliases: ["migrate-from-jekyl"]
# ShowToc: true
# TocOpen: true
# weight: 2
---

Привет!
В выпуске декомпозируем микросервисы с помощью RabbitMq, читаем мнение о Jigsaw от разработчика ByteBuddy и узнаем, что думает главный архитектор джавы насчет этого.

[https://youtu.be/ac1v5kF_FGs](https://youtu.be/ac1v5kF_FGs)

**Ask the architect with Mark Reinhold and Dan Hardiker**

Марк Рейнхольд отвечает на вопросы о Jigsaw и развеивает основные опасения насчет  в Java 9.

[https://techblog.bozho.net/spring-boot-enablewebmvc-common-use-cases/](https://techblog.bozho.net/spring-boot-enablewebmvc-common-use-cases/)

**Spring Boot, @EnableWebMvc And Common Use-Cases**

Автор разбирается как работает аннотация @EnableWebMvc в спринге.

[http://blog.codeleak.pl/2017/04/thymeleaf-3-standard-layout-system.html](http://blog.codeleak.pl/2017/04/thymeleaf-3-standard-layout-system.html)

**THYMELEAF 3 STANDARD LAYOUT SYSTEM IMPROVEMENTS**

Релиз таймлифа c 3 версии полностью переписан. Пробовал заменить вторую версию на третью и все заработало, кроме тэга <th:include>. Заменяем тэг <th:include> на <th:insert> и все работает из коробки.

[https://programmaticponderings.com/2017/05/08/decoupling-microservices-using-message-based-rpc-ipc-with-spring-rabbitmq-and-ampq/](https://programmaticponderings.com/2017/05/08/decoupling-microservices-using-message-based-rpc-ipc-with-spring-rabbitmq-and-ampq/)

**Decoupling Microservices using Message-based RPC IPC, with Spring, RabbitMQ, and AMPQ**

Чтобы микросервисы не зависили друг от друга обычно делают их "слабо связанными". Автор рассматривает один из таких способов используя Spring, RabbitMq и MongoDB.

[https://www.insaneprogramming.be/article/2017/05/01/what-i-dont-like-spring-data/](https://www.insaneprogramming.be/article/2017/05/01/what-i-dont-like-spring-data/)

**Spring Data and Clean Architecture**

Пост про удобность и неудобность модуля спринг дата для монги. Все именно так, как пишет автор, в начале — восхищение библиотекой, затем — желание избавится.

[https://www.infoq.com/presentations/performance-managed-languages](https://www.infoq.com/presentations/performance-managed-languages)

**High Performance Managed Languages**

Мартин Томпсон рассказывает про методы оптимизации приложений: про стратегии доступа к памяти, про оптимизации в рантайме, и про плюсы языков с "рантаймом"  над статически компилируемыми.

[http://mreinhold.org/blog/to-the-jcp-ec](http://mreinhold.org/blog/to-the-jcp-ec)

**An Open Letter to the JCP Executive Committee**

Компании IBM и Red Hat проголосовали против модульной системы в джаве 9 .  В ответ на это главный архитектор Java Марк Рейнхолд написал открытое письмо, в котором намекнул, что Jigsaw будет выпущена даже если комитет будет против.  Перед релизом джава 9 становится все жарче и жарче.

[http://mydailyjava.blogspot.ru/2017/05/yet-another-jigsaw-opinion-piece.html](http://mydailyjava.blogspot.ru/2017/05/yet-another-jigsaw-opinion-piece.html)

**Yet another Jigsaw opinion piece**

В продолжении обсуждения модульной системы Рафаэль Винтерхалтер, создатель известной библиотеки ByteBuddy высказывает свое мнение.

[https://www.youtube.com/watch?v=9CJ_BAeOmW0](https://www.youtube.com/watch?v=9CJ_BAeOmW0)

**Deconstructing REST Security by David Blevins**

Из доклада узнаете зачем хранить состояние аутентификации прямо в запросе.Спикер рассматривает несколько подходов к аутентификации и приходит к "идеальному" решению. В итоге «победил» Амазон и их кастомная реализация JWT.

[https://www.togglz.org/](https://www.togglz.org/)

**Togglz**

Togglz - библиотека, которая позволяет управлять фичами в приложении, по сути это набор Enum, но с удобным менеджером и контекстом.
