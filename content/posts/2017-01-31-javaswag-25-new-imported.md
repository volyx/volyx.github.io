---
author: "volyx"
title:  "Javaswag выпуск 25"
date: "2017-01-31"
# description: "Sample article showcasing basic Markdown syntax and formatting for HTML elements."
tags:  ["old-posts"]
categories: ["old-posts"]
summary: "Это первый выпуск в этом году! Выпуск немного припозднился, но дальше по расписанию. Поехали! В выпуске оживляем Skip List, разбираемся с размеров пула соединений и смотрим видео про улучшение производительности строк в Java 9."
image: ""
# series: ["Themes Guide"]
# aliases: ["migrate-from-jekyl"]
# ShowToc: true
# TocOpen: true
# weight: 2
---

Привет!
Это первый выпуск в этом году! Выпуск немного припозднился, но дальше по расписанию. Поехали!
В выпуске "оживляем" Skip List, разбираемся с размеров пула соединений и смотрим видео про улучшение производительности строк в Java 9.

[http://bruceeckel.github.io/2017/01/13/constructors-are-not-thread-safe/](http://bruceeckel.github.io/2017/01/13/constructors-are-not-thread-safe/)

**Constructors Are Not Thread-Safe**

Брюс Эккель рассуждает про потоко-небезопасные конструкторы в Java. На примерах показывает к чему это может привести, и как сделать создание объекта потокобезопасным.

[http://thenewstack.io/three-stages-software-engineering-scale/](http://thenewstack.io/three-stages-software-engineering-scale/)

**The Three Stages of Software Engineering**

Три этапа развития целей проекта - простота, эффективность, организационная структура. Такие приоритеты должны быть у компании по мнению разработчика из Линкадина. 
Если бы можно было вынести всего одно предложение из всей статьи, то это было бы "Пока ваша команда меньше 30 человек основным приоритетом должна быть простота".

[http://code.flickr.net/2017/01/05/a-year-without-a-byte/](http://code.flickr.net/2017/01/05/a-year-without-a-byte/)

**A Year Without a Byte**

Сервис flick в 2016 году ставил цель сократить расходы на хранение фотографий. Весьма амбициозная задача для фотохостинга, учитывая растущее каждый год количество загружаемого контента! Фликровцы рассказывают как пережали уже существующие фотографии, уменьшили количество резервной памяти на дисках и размеры маленьких версий фоток.

[http://ticki.github.io/blog/skip-lists-done-right/](http://ticki.github.io/blog/skip-lists-done-right/)

**Skip Lists: Done Right**

Список с пропусками, он же Skip Lists - несправедливо "забытая" структура данных в джаве. Статья поможет освежить в памяти его устройство, и напомнит случаи, когда “скип лист” будет полезен.

[https://github.com/brettwooldridge/HikariCP/wiki/About-Pool-Sizing](https://github.com/brettwooldridge/HikariCP/wiki/About-Pool-Sizing)

**About Pool Sizing**
Какой должен быть размер пула подключения к базе данных? 10000? 1000? 100? 

Если вы хоть раз задумывались над размером пула соединений к базе данных, то эта статья для вас.

[https://youtu.be/_evzaAkd594](https://youtu.be/_evzaAkd594)

**Aleksey Shipilev - String Enhancements in JDK 9**

За 20 минут Алексей Шипилев расскажет про улучшения производительности части строк в грядущей Java 9. Маст си для джава девелопера. 

[https://medium.com/@lukleDev/how-effective-java-may-have-influenced-the-design-of-kotlin-part-1-45fd64c2f974#.qzpd6ebwm](https://medium.com/@lukleDev/how-effective-java-may-have-influenced-the-design-of-kotlin-part-1-45fd64c2f974#.qzpd6ebwm)

**How "Effective Java" may have influenced the design of Kotlin — Part 1**

Немного Котлина. А именно то,какие улучшения язык Котлин впитал из Джавы.

[http://www.baeldung.com/lmax-disruptor-concurrency](http://www.baeldung.com/lmax-disruptor-concurrency)

**Concurrency with LMAX Disruptor – An Introduction**
В блоге баелдунга рассказывается о том, как устроен фреймворк дизраптор и как ему удается быть настолько быстрым. Все дело в "mechanical sympathy" — процессе когда программа работает “в унисон” с железками.
