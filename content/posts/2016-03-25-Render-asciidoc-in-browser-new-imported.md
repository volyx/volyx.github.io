---
author: "volyx"
title:  "Рендеринг asccidoc в браузере"
date: "2016-03-25"
# description: "Sample article showcasing basic Markdown syntax and formatting for HTML elements."
tags:  ["old-posts"]
categories: ["old-posts"]
summary: ""
image: ""
# series: ["Themes Guide"]
# aliases: ["migrate-from-jekyl"]
# ShowToc: true
# TocOpen: true
# weight: 2
---

Давно хотелось разобраться с этим вопросом. Ведь аскидок очень удобен и гибок. 

Посмотрите на его синтаксис и его [документацию](http://asciidoctor.org/docs/asciidoc-syntax-quick-reference/) - это просто красиво.


К сожалению аскидок командная утилита, и каждый раз генерить html файл не очень удобно.

Есть всякие превьюхи для него:

- Десктопный превью написанный на JavaFX - [asciidocfx](http://www.asciidocfx.com/)
- [Расширение для хрома](https://chrome.google.com/webstore/detail/asciidoctorjs-live-previe/iaalpfgpbocpdfblpnhhgllgbdbchmia)
- Есть расширение для [Sublime text](https://github.com/SublimeText/AsciiDoc) и [Atom](https://github.com/asciidoctor/atom-asciidoc-preview) и  [brackets](https://github.com/asciidoctor/brackets-asciidoc-preview)

Почти все они описаны [тут](http://asciidoctor.org/docs/editing-asciidoc-with-live-preview/)

Все утилиты такого рода подразумевают [WYSIWYG](https://ru.wikipedia.org/wiki/WYSIWYG) редактирование, но не решают проблему - перегенерирование документов при каждом редактировании.

Почему нельзя автоматически это делать в браузере? Ведь расширение хрома указывает на то что такая возможность есть.

И если бы получилось писать например документацию в аскидок формате и потом отображать динамически браузером это было бы здорово.

Такая возможность есть! Ладно, хватит болтовни.

> “Talk is cheap. Show me the code.”  
>>  Linus Torvalds

Весь код доступен на [гитхабе](https://github.com/volyx/asciidocjs-project) Там же приведена инструкция - какчё-куда.

И еще раз там же висит [демка](http://volyx.github.io/asciidocjs-project/)

Дальше можно полюбоваться на:

- красивую [документацию грувей](http://groovy-lang.org/operators.html), которая тоже использует аскидок;
- как [спринг переводил](https://spring.io/blog/2013/12/13/spring-s-getting-started-guides-migrated-to-asciidoctor) свои доки на аскидок
- [генерировать rest-документацию](http://blog.ninja-squad.com/2014/02/25/rest-api-doc-with-asciidoctor-and-gradle/) с помощью gradle 
- и совсем [сумасшедшее превью аскидока](http://grooscript.org/demo/asciidoctor.html) на грускрипте(именно [из-за грускрипта](http://grooscript.org/)оно сумасшедшее) 

Даже Аллен удивлен.

<blockquote class="twitter-tweet" lang="ru"><p lang="en" dir="ltr">Convert AsciiDoc using Groovy in JavaScript using Grooscript &amp; Asciidoctor.js. This is just getting crazy awesome! <a href="http://t.co/UsxUYpvDFy">http://t.co/UsxUYpvDFy</a></p>&mdash; Dan Allen (@mojavelinux) <a href="https://twitter.com/mojavelinux/status/519789486872334337">8 октября 2014</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

