---
author: "volyx"
title:  "теорема Байеса"
date: "2016-01-19"
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

![mlodinov](/images/2016/01/---------2016-01-03-21-05-22.png)

Млодинов очень увлекательно и&nbsp;доходчиво рассказывает о&nbsp;сложных математических понятиях. Очень жаль, что эта книга не&nbsp;попалась мне во&nbsp;время курса теории вероятности в&nbsp;универеситете. Она сто процентов заинтересует вас в высшей математике и просто без формул объяснит сложные термины из теории вероятности.

Самой полезной оказалась глава, посвященная условной вероятности. Вся книга читается на раз, я без сомнений  готов перечитать ее еще раз.

На&nbsp;вероятность влияет тот факт, что событие произойдет, **если** или **при условии**, что произойдут другие события. В&nbsp;этом и&nbsp;заключается [теорема Байеса](https://ru.wikipedia.org/wiki/%D0%A2%D0%B5%D0%BE%D1%80%D0%B5%D0%BC%D0%B0_%D0%91%D0%B0%D0%B9%D0%B5%D1%81%D0%B0) или теория условной вероятности. Теорема Бернулли решает следующий вопрос: сколько получится орлов, если планируется произвести много бросков идеальной монеты, в&nbsp;то&nbsp;время как Байес исследовал первоначальную цель Бернулли&nbsp;&mdash; вопрос о&nbsp;том, насколько можно быть уверенным в&nbsp;том, что монета идеальна, если выпадает определенное число орлов. Байес разработал условную вероятность в&nbsp;попытке ответить на&nbsp;тот&nbsp;же вопрос, который увлек Бернулли: как по&nbsp;известному факту события вычислить вероятность того, что оно было вызвано данной причиной? 

Представим, что ваш босс стал отвечать на&nbsp;ваши электронные письма с&nbsp;запозданием. Многие подумают, что это конец, и&nbsp;скоро начальник вас уволит. Подумают они это потому что: если вас собираются уволить, велика вероятность того, что босс перестанет отвечать на&nbsp;ваши письма оперативно. Однако босс может запаздывать с&nbsp;ответом и&nbsp;потому что просто занят. 
Так что вероятность того что вас скоро уволят, если начальник стал отвечать на&nbsp;письма с&nbsp;задержкой, **гораздо ниже**, чем вероятность того, что ваш начальник станет отвечать на&nbsp;письма с&nbsp;задержкой если вас ждет увольнение.

Своей привлекательностью многие теории заговоров обещаны неправильному пониманию вышеприведенных логических выкладок. То&nbsp;есть все дело в&nbsp;путанице: вероятность того, что ряд событий произойдет, **если** события эти являются результатом тайного заговора, путают с&nbsp;вероятностью того, что тайный заговор существует, **если** имеет место ряд событий.

На&nbsp;вероятность влияет тот факт, что событие произойдет, **если** и&nbsp;**при условии, что** произойдут другие события.

Представьте себе компанию людей, незнакомых друг другу. И&nbsp;один из&nbsp;них неожиданно начинает нести ерунду. Кто-то из&nbsp;компании в&nbsp;шутку говорит: 
&mdash;&nbsp;&laquo;Он, наверное, спятил.&raquo;
Условная вероятность может ответить на&nbsp;этот вопрос. Насколько &laquo;наверное&raquo;? Какова вероятность того, что в&nbsp;компании сумасшедший&nbsp;и, что именно сейчас в данный момент он&nbsp;несет чушь?

Чтобы разобраться лучше, посмотрим на задаче о двух девочках.

> В&nbsp;семье двое детей; какова вероятность того, что если один из&nbsp;детей &mdash;
девочка, то&nbsp;и&nbsp;другой ребенок тоже девочка? 

В&nbsp;этой задаче пространство элементарных событий изначально такое:
 
* (мальчик, мальчик),
* (мальчик, девочка),
* (девочка, мальчик),
* (девочка, девочка),

Однако оно сокращается до следующих параметров, так как мы уже знаем что один ребенок - девочка: 

* (мальчик, девочка), 
* (девочка, мальчик), 
* (девочка, девочка), 

Получается, что если вы узнаете, что один из&nbsp;детей&nbsp;&mdash; девочка, что шансы на&nbsp;семью из&nbsp;двух девочек составляют 1&nbsp;из&nbsp;3.

А теперь представьте, что Млодинов дальше утверждает:

> Тот факт, что одну из девочек зовут Флорида, меняет шансы на 1 из 2. 

Кажется совершенно невероятным. Видимо, в имени Флорида есть что-то особенное. Давайте разбираться. Итак, условие:

> В&nbsp;семье двое детей; какова вероятность того, что если один из&nbsp;детей &mdash;
девочка по&nbsp;имени Флорида, то&nbsp;и&nbsp;другой ребенок тоже девочка? 

В этой задаче нас интересует помимо пола детей еще и&nbsp;имя,
поскольку речь о&nbsp;девочках. Наше первоначальное пространство элементарных событий должно
включать в&nbsp;себя все вероятности, поэтому список содержит и&nbsp;пол, и&nbsp;имя. Обозначим девочку по
имени Флорида как &laquo;девочка&nbsp;Ф&raquo;, а&nbsp;девочку по&nbsp;имени не&nbsp;Флорида как &laquo;девочка не&nbsp;Ф&raquo;.
Обозначим пространство элементарных событий:

* (мальчик, мальчик)
* (мальчик, девочка Ф.)
* (мальчик, девочка не&nbsp;Ф.)
* (девочка&nbsp;Ф., мальчик)
* (девочка не&nbsp;Ф., мальчик)
* (девочка не&nbsp;Ф., девочка Ф.)
* (девочка&nbsp;Ф., девочка не&nbsp;Ф.)
* (девочка не&nbsp;Ф., девочка не&nbsp;Ф.)
* (девочка&nbsp;Ф., девочка Ф.).

Теперь &laquo;урежем&raquo;. Так как нам известно, что один из&nbsp;детей&nbsp;&mdash; девочка по&nbsp;имени Флорида, можно сократить пространство элементарных событий:

* (мальчик, девочка Ф.)
* (девочка&nbsp;Ф., мальчик)
* (девочка не&nbsp;Ф., девочка Ф.)
* (девочка&nbsp;Ф., девочка Ф.)

Теперь видно, чем еще эта задача отличается от&nbsp;задачи про двух дочерей. Поскольку утверждения, что девочку
зовут Флорида и&nbsp;девочку зовут не&nbsp;Флорида, нельзя назвать равновероятными, не&nbsp;являются
таковыми и&nbsp;все элементы пространства элементарных событий.

В&nbsp;1935, последнем году, за&nbsp;который Управление социальным обеспечением предоставило
статистику в&nbsp;отношении имени, около 1&nbsp;из&nbsp;30.000 девочек были наречены именем
Флорида. Поскольку имя становилось все менее популярным, предположим, что сегодня
вероятность появления девочки по&nbsp;имени Флорида равна 1&nbsp;из&nbsp;1&nbsp;млн. Это значит следующее:
если нам станет известно, что определенную из&nbsp;двух девочку зовут не&nbsp;Флорида, ничего
страшного, однако если мы&nbsp;узнаем, что ее&nbsp;зовут Флорида, можно сказать, что мы&nbsp;попали в
точку. Вероятность того, что обеих девочек назовут именем Флорида (даже если мы
проигнорируем тот факт, что обычно родители избегают давать детям одинаковые имена),
настолько мала, что можно спокойно ею&nbsp;пренебречь. Итак, вот что у&nbsp;нас остается: 

* (мальчик, девочка&nbsp;Ф.)
* (девочка&nbsp;Ф., мальчик)
* (девочка не&nbsp;Ф., девочка&nbsp;Ф.)
* (девочка&nbsp;Ф., девочка не&nbsp;Ф.). 

Все эти события в&nbsp;весьма хорошем приближении равновозможны.

Поскольку 2&nbsp;из&nbsp;4, то&nbsp;есть половина элементов пространства элементарных событий
являются семьями с&nbsp;двумя девочками, ответом не&nbsp;может быть 1&nbsp;из&nbsp;3&nbsp;&mdash; как это было в&nbsp;задаче с
двумя дочерьми,&nbsp;&mdash; ответом является 1&nbsp;из&nbsp;2. Все дело в&nbsp;дополнительной информации &mdash;
осведомленности насчет имени девочки.

Если вы&nbsp;по-прежнему теряетесь в&nbsp;догадках, то&nbsp;можно представить себе следующее: в
очень-очень большой комнате мы&nbsp;собираем 75&nbsp;млн семей с&nbsp;двумя детьми, из&nbsp;которых хотя&nbsp;бы
один ребенок&nbsp;&mdash; девочка. Как нам стало известно из&nbsp;задачи с&nbsp;двумя дочерьми, в&nbsp;комнате
окажется около 25&nbsp;млн семей с&nbsp;двумя девочками и&nbsp;50&nbsp;млн семей с&nbsp;одной девочкой (25&nbsp;млн
семей, в&nbsp;которых девочка является старшим ребенком, и&nbsp;столько&nbsp;же семей, в&nbsp;которых девочка
является младшим ребенком). 

Далее &laquo;урезаем&raquo;: просим остаться в&nbsp;комнате только те&nbsp;семьи, в
которых есть девочки по&nbsp;имени Флорида. Поскольку Флорида&nbsp;&mdash; 1&nbsp;имя на&nbsp;1&nbsp;млн имен,
останутся около 50&nbsp;из&nbsp;50&nbsp;млн семей с&nbsp;одной девочкой. А&nbsp;из&nbsp;25&nbsp;млн семей с&nbsp;двумя девочками 50
тоже останутся: 25&nbsp;потому, что их&nbsp;первый ребенок назван по&nbsp;имени Флорида, другие 25&nbsp;потому,
что их&nbsp;младшая дочь названа Флоридой. 

В&nbsp;этом примере всех девочек можно представить как
лотерейные билеты; в&nbsp;таком случае девочки по&nbsp;имени Флорида станут выигрышными билетами.
И&nbsp;хотя семей, в&nbsp;которых один из&nbsp;двух детей&nbsp;&mdash; девочка, в&nbsp;два раза больше, чем семей, в&nbsp;которых
оба ребенка&nbsp;&mdash; девочки, семьи с&nbsp;двумя девочками обладают двумя лотерейными билетами,
поэтому среди выигравших будет примерно одинаковое соотношение семей с&nbsp;одной девочкой и
семей с&nbsp;двумя девочками.

Следовательно, ответ 1/2. Если в семье одну девочку зовут Флорида, то вероятность, того что второй ребенок девочка - 1/2.