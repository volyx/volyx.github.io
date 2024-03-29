---
author: "volyx"
title:  "Javaswag выпуск 22"
date: "2016-11-24"
# description: "Sample article showcasing basic Markdown syntax and formatting for HTML elements."
tags:  ["old-posts"]
categories: ["old-posts"]
summary: "Привет! В выпуске стримим данные из MySql с помощью Spring Data, разбираемся с производительностью JVM в докере и знакомимся с проектом Reactor от Spring."
image: ""
# series: ["Themes Guide"]
# aliases: ["migrate-from-jekyl"]
# ShowToc: true
# TocOpen: true
# weight: 2
---

Привет!

В выпуске стримим данные из MySql с помощью Spring Data, разбираемся с производительностью JVM в докере и знакомимся с проектом Reactor от Spring. 

[https://medium.com/@johnmcclean/trampolining-a-practical-guide-for-awesome-java-developers-4b657d9c3076#.gqjbui9qd](https://medium.com/@johnmcclean/trampolining-a-practical-guide-for-awesome-java-developers-4b657d9c3076#.gqjbui9qd)

**Trampolining: a practical guide for awesome Java Developers**

Основная проблема рекурсивных методов это зависимость от размера стека. С помощью рекурсии можно обрабатывать только небольшие объемы данных, чтобы не поймать StackOverFlowError. Но когда мы переписываем код с рекурсии на очередь например, код становится не таким читаемым. В статье рассказывается о том как можно писать рекурсивный код, который будет выполнятся итеративно.

[http://mrhaki.blogspot.ru/2014/05/groovy-goodness-implementing-traits-at.html](http://mrhaki.blogspot.ru/2014/05/groovy-goodness-implementing-traits-at.html)

**Groovy Goodness: Implementing Traits at Runtime**

В статье рассказывается про Трейты — конструкцию из языка Груви. Трейт — это интерфейс, который мы можем добавить к классу динамически. Мы как будто подмешиваем свое поведение к уже существующему классу.

[https://knes1.github.io/blog/2015/2015-10-19-streaming-mysql-results-using-java8-streams-and-spring-data.html](https://knes1.github.io/blog/2015/2015-10-19-streaming-mysql-results-using-java8-streams-and-spring-data.html)

**Streaming MySQL Results Using Java 8 Streams and Spring Data JPA**

В статье рассказывается о том как можно отдавать данные из MySql в потоковом режиме. Углубившись в дебри документации к MySql  автору удалось сократить время экспорта с **137 секунд до 9! **

[http://codeahoy.com/2016/11/16/performance-testing-serverside-applications/](http://codeahoy.com/2016/11/16/performance-testing-serverside-applications/)

**Performance Testing Serverside Applications**

В статье рассказывается как нужно и как не нужно тестировать производительность приложения. Из статьи узнаете почему бессмысленно мерить производительность приложения не в продакшн окружении.

[https://techblog.bozho.net/hardcode-server-ip-apps/](https://techblog.bozho.net/hardcode-server-ip-apps/)

**Domain Fallback Mechanism In Apps**

Что делать если какой-то из больших днс серверов упал? Да, теперь мы не можем подключится к серверу по его домену, а в наше время микросервисов это еще более больно, чем раньше. Автор решает эту проблему с помощью фолбеков - сначала мы пробуем первый домен, если не получается запасной, затем пробуем достучаться по ip адресу.

[http://javarticles.com/2016/11/linkedblockingqueue-example.html](http://javarticles.com/2016/11/linkedblockingqueue-example.html)

**LinkedBlockingQueue Example**

Автор с отличными примерами и картинками рассказывает о том как работает ‘LinkedBlockingQueue ’ Обязательно запустите примеры из статьи - они хорошо демонстрируют применение этой структуры данных.

[https://www.youtube.com/watch?v=6ePUiQuaUos&t=310s&index=47&list=WL](https://www.youtube.com/watch?v=6ePUiQuaUos&t=310s&index=47&list=WL)

**The JVM and Docker. A good idea? by Christopher Batey**

Кристофер рассказывает о проблемах запуска приложения в Докер контейнере и об инструментах, с помощью которых можно мониторить состояние приложений.
Вы знали, например, что если запустить несколько контейнеров с Jetty приложение может неожиданно упасть ¯\_(ツ)_/¯ ! Не забывайте смотреть настройки библиотек по умолчанию!

[https://www.quora.com/Which-is-better-Play-Framework-or-Spring-MVC-How-should-I-decide-what-to-use](https://www.quora.com/Which-is-better-Play-Framework-or-Spring-MVC-How-should-I-decide-what-to-use)

**Which is better, Play Framework or Spring MVC? How should I decide what to use?**

Отличный ответ с Quora, который претендует на целый пост. О том почему Линкадин перешел со Спринга на Плэй Фреймворк. Вкратце — Спринг очень сложный. Концепции простые, но сложно подружить все его компоненты вместе в рамках большого приложения.

[http://musigma.org/java/2016/11/21/reactor.html](http://musigma.org/java/2016/11/21/reactor.html)

**Reactive systems using Reactor**

На смену хайпу про микросервисы приходит "новая" модная парадигма — реактивность. Теперь мы пишем не просто микросервисы, а реактивные микросервисы. На основе библиотеки Reactor автор рассказывает об основных концепциях реактивных стримов. Реактивность скоро появится в Спринге 5.0 — всем читать и разбираться.

[http://upli.st/l/list-of-all-ascii-emoticons](http://upli.st/l/list-of-all-ascii-emoticons)

Сегодня десерт. Ссылка самые популярные текстовые эмодзи - чтобы в чате быть на высоте ( ͡° ͜ʖ ͡°)
