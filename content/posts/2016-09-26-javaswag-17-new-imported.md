---
author: "volyx"
title:  "Javaswag выпуск 17"
date: "2016-09-28"
# description: "Sample article showcasing basic Markdown syntax and formatting for HTML elements."
tags:  ["old-posts"]
categories: ["old-posts"]
summary: "В выпуске видео с JavaOne 2016, модульность в Java 9 и оптимизации JVM."
image: ""
# series: ["Themes Guide"]
# aliases: ["migrate-from-jekyl"]
# ShowToc: true
# TocOpen: true
# weight: 2
---

Привет!
В выпуске 

[Asynchronous timeouts with CompletableFutures in Java 8 and Java 9](http://iteratrlearning.com/java9/2016/09/13/java9-timeouts-completablefutures.html)

В Java 9 `CompletableFuture` получит несколько методов для асинронной работы с таймаутами: `orTimeout`, `completeOnTimeout`, которые особенно пригодятся если если один из ваших вызовов внутри `CompletableFuture` не отвечает или завис.

[JavaOne 2016](https://www.youtube.com/playlist?list=PLPIzp-E1msrYicmovyeuOABO4HxVPlhEA)

Видео с JavaOne - для тех кто хочет быт ьна самой передовой. Темы с JavaOne обычно расползаются по конференциям и задают тренд на следущий год.


[Consumer In Place Of Returning List](https://arnaudroger.github.io/blog/2016/09/19/consumer-in-place-of-returning-list.html)

Что если в метод передавать не `List`, а `Consumer`? Это избавит от создания списка, который в будущем может не пригодится. 

[The Safe Builder Pattern](http://www.radicaljava.com/2016/09/19/safe-builder.html)

Самый популярный подход для созднания сложных объектов - паттерн `Builder`, но его недостатком является то, что нельзя проверить на этапе компиляции - все параметры ьыли установлены. Поэтому часто можно неожиданно поймать `NullPointerExcetion`. В статье рассказывается, как реализовать паттерн `Builder` без этого недостатка. 


[Complete Guide: Inheritance strategies with JPA and Hibernate](http://www.thoughts-on-java.org/complete-guide-inheritance-strategies-jpa-hibernate/)

В статье рассказывается о 4 стратегиях, поддерживаемых `Hibernate` для храниия объектов с иерархией. "Must read" для всех у кого проекте используется `Hibernate`.


[Hibernate испортил ваш проект? Нет, это были вы!](http://xpinjection.com/articles/hibernate-ruined-your-project-no-it-was-you/)

В статье три полезных видео рассказывающих об устройстве `Hibernate`, о сложностях испольхования и о пролемах с проиводительностью. Все три видео на русском языке.



Еженедельные выпуски Джавасвэга на почту — [http://javaswag.curated.co](http://javaswag.curated.co).

Еженедельные выпуски Джавасвэга в Телеграме — [http://telegram.me/javaswag](http://telegram.me/javaswag).

Удачи!
