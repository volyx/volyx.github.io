---
author: "volyx"
title:  "Написать функцию, переворачивающую строку без использования дополнительной памяти"
date: "2016-03-13"
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

[Задача](https://www.interviewcake.com/question/javascript/reverse-string-in-place)

Мы будем менять первый и последний элемент, затем второй и второй с конца, и так далее пока не достигнем середины.

{% highlight java %}
  public String reverse(String str) {

    char[] strChars = str.toCharArray();

    int startIndex = 0;
    int endIndex = strChars.length - 1;

    while (startIndex < endIndex) {

        // swap characters
        char temp = strChars[startIndex];
        strChars[startIndex] = strChars[endIndex];
        strChars[endIndex] = temp;

        // move towards middle
        startIndex++;
        endIndex--;
    }

    return new String(strChars);
}
{% endhighlight %}

Сложность
`O(n)` по времени и `O(1)` по доп. месту.


