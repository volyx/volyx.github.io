---
author: "volyx"
title:  "Javaswag выпуск 29"
date: "2017-04-07"
# description: "Sample article showcasing basic Markdown syntax and formatting for HTML elements."
tags:  ["old-posts"]
categories: ["old-posts"]
summary: "В выпуске создаем докер контейнеры на все случаи жизни, разбираемся с отличиями реактивных систем и ставим себе мавен-плагин для отображения времени выполнения."
image: ""
# series: ["Themes Guide"]
# aliases: ["migrate-from-jekyl"]
# ShowToc: true
# TocOpen: true
# weight: 2
---

Всем привет!
В выпуске создаем докер контейнеры на все случаи жизни, разбираемся с отличиями реактивных систем и ставим себе мавен-плагин для отображения времени выполнения.

[https://www.voxxed.com/blog/interview/java-9-coming-nicolai-parlog/](https://www.voxxed.com/blog/interview/java-9-coming-nicolai-parlog/)

**Java 9 is coming! – Nicolai Parlog**

Будем смотреть видео про модули из джава 9, пока не поймем чем они полезны разработчикам. 

[https://codefresh.io/blog/java_docker_pipeline/](https://codefresh.io/blog/java_docker_pipeline/)

**Crafting perfect Java Docker build flow**

Автор рассказывает, как с нуля создать докер контейнеры для джава приложения. Всего три вида контейнеров — для продакшена, для сборки и тестов, для интеграционных тестов. Узнаете как создать свой докер контейнер с линуксом размером всего 170 мегабайт. 

[https://www.reactivesystems.eu/2017/01/31/things-i-wish-i-knew-when-i-started-building-reactive-systems.html](https://www.reactivesystems.eu/2017/01/31/things-i-wish-i-knew-when-i-started-building-reactive-systems.html)

**Things I Wish I Knew When I Started Building Reactive Systems**

Строить реактивную архитектуру нужно совершенно иначе, чем монолитную. Об отличиях этой архитектуры и о чем желательно подумать заранее в статье.

[https://blog.hackeriet.no/detect-security-holes-during-build/](https://blog.hackeriet.no/detect-security-holes-during-build/)

**Detect security problems at compile time**

Плагин для мавена который "проверяет" зависимости  на уязвимости. Не сам конечно, а просто сверяет версии библиотек со списком тех, в которых найдены критичные баги.  Используя плагин можно наконец объяснить своему ПМу почему стоит обновиться на новую версию библиотеки.

**[https://marutsingh.com/2017/03/17/vert-x-master-worker-microservices**/](https://marutsingh.com/2017/03/17/vert-x-master-worker-microservices/)

**VERT.X MASTER WORKER ARCHITECTURE**

Простой пример использования vert.x. В примере автор создает мастер сервис, и несколько сервисов, которые обрабатывают "задания" от мастера.

**[https://github.com/timgifford/maven-buildtime-extensio**n](https://github.com/timgifford/maven-buildtime-extension)

# **maven-buildtime-extension**

Мавен плагин, который пишет сколько времени выполнялась каждая цель.

[https://www.infoq.com/presentations/etl-streams](https://www.infoq.com/presentations/etl-streams)

**ETL Is Dead, Long Live Streams**

Спикер предлагает пересмотреть архитектуру приложения, и представить все взаимодействие компонентов программы через очередь сообщений. В роли очереди выступает Apache Kafka. 

[https://zupzup.org/java-0-deps-webapp/](https://zupzup.org/java-0-deps-webapp/)

**Zero Dependencies Web-App in Java**

Пишем простой Http сервер не используя никаких дополнительных библиотек.

Пройти опрос.

[https://goo.gl/forms/J1y8QOHCUkb3SXX13](https://goo.gl/forms/J1y8QOHCUkb3SXX13)

По данным разных исследований доля женщин в ИТ-индустрии на данный момент составляет не более 10-20%. Почему же так мало женщин в сфере компьютерных разработок, какова основная причина? Этот вопрос ставит перед собой Анна Камнева, студентка 4 курса факультета социологии СПбГУ. Дорогие женщины-программисты, помогите ей разобраться, пройдя подготовленный ею соцопрос. Чуть позже мы опубликуем результаты исследования на «Хабре», уверены, всем будет очень интересно! 
