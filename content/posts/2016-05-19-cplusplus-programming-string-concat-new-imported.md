---
author: "volyx"
title:  "Склейка строк"
date: "2016-05-19"
# description: "Sample article showcasing basic Markdown syntax and formatting for HTML elements."
tags:  ["old-posts"]
categories: ["old-posts"]
summary: "Вам требуется реализовать функцию конкатенации (склейки) двух C-style строк. Функция конкатенации принимает на вход две C-style строки и дописывает вторую в конец первой так, чтобы первая строка представляла из себя одну C-style строку равную конкатенации двух исходных."
image: ""
# series: ["Themes Guide"]
# aliases: ["migrate-from-jekyl"]
# ShowToc: true
# TocOpen: true
# weight: 2
---

Задание 

[https://stepic.org/lesson/Использование-указателей-540/step/7](https://stepic.org/lesson/Использование-указателей-540/step/7)

Вам требуется реализовать функцию конкатенации (склейки) двух C-style строк. Функция конкатенации принимает на вход две C-style строки и дописывает вторую в конец первой так, чтобы первая строка представляла из себя одну C-style строку равную конкатенации двух исходных. 

Не забудьте, что в результирующей строке должен быть только один нулевой символ — тот, что является маркером конца строки. 

Гарантируется, что в первой строке достаточно памяти (т.е. она располагается в массиве достаточной длины), чтобы разместить конкатенацию обеих строк, но не больше.

Требования к реализации: при выполнении задания вы можете определять любые вспомогательные функции, если они вам нужны. Выводить или вводить что-либо не нужно. Функцию main определять не нужно.

Решение

{% highlight cpp %}
#include <iostream>
using namespace std;

unsigned strlen(const char *str)
{   
	unsigned i = 0;
	for (; *str != '\0'; str++) 
	{	
		i++;
		
	}
	return  i;
}

void strcat(char *to, const char *from)
{
    unsigned i = strlen(to);
	for (; *from != '\0' ; from++) 
	{	
		to[i] = from[0];
		i++;
	}
	to[i] = '\0';
}

int main() {
	char s[] = "Hello ";
	char s1[] = "World!";
	strcat(s, s1);
    cout << s << endl;
}
{% endhighlight %}

Сам курс [https://stepic.org/course/7](https://stepic.org/course/7)