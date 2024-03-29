---
author: "volyx"
title:  "Первый релиз в Maven Central"
date: "2015-08-26"
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
 
![](/images/sonatype.png)

Основная мысль RTFM!

Единственный верный и правильный мануал по публикации в централ - ((http://central.sonatype.org/pages/apache-maven.html)), остальное все - чушь и старье. Надолго запомню, что читать нужно только официальную документацию - все остальное - не актуально. Потратил на этой ерунде долгие 2 часа, а когда нашел мануал - справился за 15 минут. Хотя нужно быть честным - и пока автоматически у меня не получилось "релизнуть". Заходил в ((https://oss.sonatype.org)) и загружал библиотеки руками.

Теперь с нетерпением жду когда мое творенье, а точнее  сказать просто форкнутое чужое творенье появится в центральном репозиториии. А звучит то как - *"в Центральном!"*.

![](/images/update-maven.gif)

Итак про форкнутую библиотеку, если говорить по русски - то стыренную, а именно:

- скомпилированную;
- выложенную в централ;


Но стыренную официально с подтверждением, а точнее с отсутсвием такого от самого владельца.

![](/images/email-mongeez.png)

Так что совесть моя чиста. А тем временем скачать ее хотели многие, судите сами:

![](/images/mongeez-issues.png)

[Источник](https://github.com/secondmarket/mongeez/issues/50)

Похоже пока заинтересованные люди работали в компании её поддерживали, а потом перестали, в то время как монга только развивалась и обрастала новыми инструментами.

![](/images/mongeez-commits.png)

Новый дом библиотеки теперь тут - (https://github.com/volyihin/mongeez). Скачать можно так:

{% highlight xml %}
<code>
<dependency>
  <groupId>com.github.volyihin</groupId>
  <artifactId>mongeez</artifactId>
  <version>0.9.5</version>
</dependency>
</code>
{% endhighlight %}

А вот и в самом централе:

![](/images/maven-central.png)

*Update:*
Мне только что пришло письмо от Олексия.

![](/images/mongeez-answer.png)

И вот теперь встала дилемма. С одной стороны релиз сделан, и мне не сильно нужна помощь, с другой стороны - совесть.

![](/images/dreaminess.jpg)