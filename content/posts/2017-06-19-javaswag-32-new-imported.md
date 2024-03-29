---
author: "volyx"
title:  "Javaswag выпуск 32"
date: "2017-06-19"
# description: "Sample article showcasing basic Markdown syntax and formatting for HTML elements."
tags:  ["old-posts"]
categories: ["old-posts"]
summary: "В выпуске смотрим как Марк Рейнхольд рефакторит проект к джаве 9, изучаем новую утилиту jstat и разбираемся почему решения для Гугла не подходят маленьким приложениям."
image: ""
# series: ["Themes Guide"]
# aliases: ["migrate-from-jekyl"]
# ShowToc: true
# TocOpen: true
# weight: 2
---

Привет!

В выпуске смотрим как Марк Рейнхольд рефакторит проект к джаве 9, изучаем новую утилиту jstat и разбираемся почему решения для Гугла не подходят маленьким приложениям.

[https://youtu.be/GkP83hvdeMk](https://youtu.be/GkP83hvdeMk)

**Real World Java 9 by Trisha Gee**

Триша Ги, девелопер-адвокат из компании Jetbrains показывает, как отрефакторить приложение с восьмой джавы на девятую. Триша пишет код в Inteliji IDEA, в которой уже есть поддержка новых фич.

[https://youtu.be/czhSo8rotC4](https://youtu.be/czhSo8rotC4)

**Migrating to Modules by Mark Reinhold**

Архитектор джавы Марк Рейнхольд показывает как разбить существующее приложение на модули. Марк в отличие от Триши пишет код в консоли и собирает проект через коммандную строку. Интересно наблюдать как пишет на джаве архитектор джавы.

**[http://marxsoftware.blogspot.ru/2017/05/jvm-statistics-with-jstat.htm**l](http://marxsoftware.blogspot.ru/2017/05/jvm-statistics-with-jstat.html)

**JVM Statistics with jstat**

Автор рассказывает о новой утилите для просмотра статистики - ** **jstat.  Утилита появится в Java 9. Возникает вопрос зачем она нужна? Ведь все данные из jstat мы можем посмотреть через VisualVM, gc:logs. Дело в том, что теперь с помощью jstat мы сможем подключаться уже к работающей виртуальной машине, и "на лету" доставать параметры, которые раньше были доступны только, если сконфигурировать их заранее.  Большой плюс ещё и в том, что все это можно делать из командной строки. За параметрами и примерами использования — в статью.

[https://medium.com/@magnus.chatt/why-you-should-totally-switch-to-kotlin-c7bbde9e10d5](https://medium.com/@magnus.chatt/why-you-should-totally-switch-to-kotlin-c7bbde9e10d5)

**Why you should totally switch to Kotlin**

Котлин нехило хайпанул после Google IO, где его объявили официальным языком для написания приложений для андройда. Благодаря этому, интернет наводнили десятки статей о том «нужен ли Котлин», «Котлин не нужен», «Почему следует использовать Котлин». Конечно, лучше самому написать на котлине пару хеллоу-ворлдов, но если нет времени то - можно прочесть статью. В ней автор проходится по фичам языка, и рассказывает чем язык так хорош. 

[https://plumbr.eu/blog/performance-blog/the-use-of-proxy-indicators-in-service-management](https://plumbr.eu/blog/performance-blog/the-use-of-proxy-indicators-in-service-management)

**The use of proxy indicators in service management**

Статья о том как SLA приложения зависит от длины очереди, по каким метрикам команда Plumbr мониторит длину очередей между микросервисами и как они к этому пришли.

[https://www.infoq.com/articles/Finalize-Exiting-Java](https://www.infoq.com/articles/Finalize-Exiting-Java)

**Under The Hood with the JVM's Automatic Resource Management**

Метод finalize() пришел в Java из С++ из паттерна RAII(Resource Acquisition Is Initialization) Автор рассказывает о том: как метод finalize() появился в джаве.

**[https://blog.bradfieldcs.com/you-are-not-google-84912cf44af**b](https://blog.bradfieldcs.com/you-are-not-google-84912cf44afb)

**You Are Not Google**

Вашим данным скорее всего подойдет обычная SQL база данных. Не согласны? Добро пожаловать в статью, в которой автор рассказывает почему вам не нужны большинство популярных highload решений.

**[http://sgiz.mobi/s3/63243b734400** ](http://sgiz.mobi/s3/63243b734400)

**Опрос**

Напоследок, опрос о работодателях от группы студентов факультета социологии СПбГУ. Они проводят исследование рейтинга IT работодателей Санкт-Петербурга и Москвы. Опрос займет 5 минут. Обязательно приложим результаты опроса. Либо вы увидите их сами на habrahabr.ru в блоге "Моего круга" и в группе https://vk.com/jugru.
