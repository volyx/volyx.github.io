---
author: "volyx"
title:  "Javaswag выпуск 24"
date: "2016-12-16"
# description: "Sample article showcasing basic Markdown syntax and formatting for HTML elements."
tags:  ["old-posts"]
categories: ["old-posts"]
summary: "Привет! В выпуске ограничиваем скорость загрузки с сервера, кэшируем данные из монги в редисе и разбираемся со статической компиляцией в Джаве 9."
image: ""
# series: ["Themes Guide"]
# aliases: ["migrate-from-jekyl"]
# ShowToc: true
# TocOpen: true
# weight: 2
---

Привет! В выпуске ограничиваем скорость загрузки с сервера, кэшируем данные из монги в редисе и разбираемся со статической компиляцией в Джаве 9.

[https://dzone.com/articles/enabling-caching-in-mongodb-database-with-redis-us](https://dzone.com/articles/enabling-caching-in-mongodb-database-with-redis-us)

**Caching in MongoDB With Redis Using Spring Boot**

В статье рассказывается, как можно ускорить работу с монгой, подключив редис кэш, "без регистрации и смс", точнее без XML конфигурации. 

[https://blog.twitter.com/2016/simplify-service-dependencies-with-nodes](https://blog.twitter.com/2016/simplify-service-dependencies-with-nodes)

**Simplify Service Dependencies with Nodes**

Инженеры из твиттера рассказывают о том как они боролись с ростом количества запросов к "микросервисам поиска" в приложении. В статье — сражение с циклическими зависимостями данных, асинхронные запросы, собственная опенсорс библиотека Finagle.

[http://jug.ru/2016/12/aot-hotspot/](http://jug.ru/2016/12/aot-hotspot/)

**Время компилировать: Дмитрий Чуйко и Никита Липский про AOT в HotSpot**

Статическая компиляция семимильными шагами приходит и в Джава мир. О том для чего она нужна и как все это связано с лозунгом Джава "Write once - run anywhere".
Дисклеймер - Джава идет в сторону iOS, но это не точно. 

Кстати, эту статью написал и прислал подписчик. Если у вас есть чем поделиться с любителями джавы, не стесняйтесь присылать ссылки на почту волыхингмэйл

[https://plumbr.eu/blog/monitoring/time-in-distributed-systems](https://plumbr.eu/blog/monitoring/time-in-distributed-systems)

**Time in distributed systems**

Инженеры из Пламбр рассказывают о том, как они синхронизируют время в своих джава агентах. Решение позаимствовано из распределенных систем и будет полезно всем кто интересуется этой темой.

[http://book.mixu.net/distsys/single-page.html](http://book.mixu.net/distsys/single-page.html)

**Distributed systems ****for fun and profit**
Джава мир продолжает двигаться в сторону микросервисов и такие термины как пропускная способность, скорость отклика, отказоустойчивость приходят в джаву из распределенных систем. В ссылке небольшая книга о концепциях и терминах распределенных систем. 

[http://martin.kleppmann.com/2012/12/05/schema-evolution-in-avro-protocol-buffers-thrift.html](http://martin.kleppmann.com/2012/12/05/schema-evolution-in-avro-protocol-buffers-thrift.html)

**Schema evolution in Avro, Protocol Buffers and Thrift**

Представьте, что у вас есть несколько микросервисов, которые обмениваются между собой сообщениями. Что вы будете делать если понадобилось добавить поле в одно из сообщений и при этом нельзя перезапускать все микросервисы? Решение есть. Ваши сообщения должны поддерживать "эволюцию схемы" - то есть работать только с теми полями, о которых они знают, а “устаревшие” не использовать.

Мартин Клеппман рассказывает о том как с этой проблемой справились в библиотеках Avro, Protocol Buffers, Thrift.

[https://ivanyu.me/blog/2016/12/12/about-akka-streams/](https://ivanyu.me/blog/2016/12/12/about-akka-streams/)

**About Akka Streams**

Автор рассказывает о том как с помощью Акка Стримов можно декларативно конструировать асинхронные "пайпайны" для обработки данных. Автор простым языком объясняет концепции, которые за этим всем стоят.

[http://www.nurkiewicz.com/2015/06/writing-download-server-part-i-always.html?m=1](http://www.nurkiewicz.com/2015/06/writing-download-server-part-i-always.html?m=1)

**Writing a download server. Part I: Always stream, never keep fully in memory**

Если бы я мог вернуться в прошлое, я передал бы себе следующее послание - "Не клади все данные из файла в массив байтов - используй стримы". Однажды я

столкнулся с похожим вопросом на собеседовании и провалил тестовое задание.  Читайте статью и не делайте как я.

[http://www.nurkiewicz.com/2011/03/tenfold-increase-in-server-throughput.html](http://www.nurkiewicz.com/2011/03/tenfold-increase-in-server-throughput.html)

**Tenfold increase in server throughput with Servlet 3.0 asynchronous processing**

Представьте, что у вашего приложения появился очень активный пользователь, который только и делает что загружает файлы с вашего сервера. Остальным пользователям перестает хватать скорости и сервер начинает тратить много памяти и процессора. Одно из возможных решений это ограничить скорость загрузки с сервера, или сделать ее контролируемой. Томас рассказывает, как написать сервлет, который будет отдавать файлы с одной и той же скоростью, независимо от того сколько пользователей к нему подключилось.
