---
author: "volyx"
title:  "Замыкания"
date: "2014-11-18"
# description: "Sample article showcasing basic Markdown syntax and formatting for HTML elements."
tags:  ["old-posts"]
categories: ["old-posts"]
summary: "Добавить новое поведение в существующий метод легко, но часто это бывает не совсем верным решением. Когда изначально создается какой-то метод, то он обычно делает строго одно действие. Любое добавление нового кода выглядит немного подозрительно. Скорее всего, вы добавляете новый код, потому что хотите, чтобы он выполнялся в одно время с уже существующим кодом."
image: "../img/closure.jpg"
# series: ["Themes Guide"]
# aliases: ["migrate-from-jekyl"]
# ShowToc: true
# TocOpen: true
# weight: 2
---

Если посмотреть определени замыкания в link:http://bit.ly/15CgKnT[википедии], то мы увидем следующее:

.Замыкание
****
Замыкание (англ. closure) в программировании — функция, в теле которой присутствуют ссылки на переменные, объявленные вне тела этой функции в окружающем коде и не являющиеся её параметрами. Говоря другим языком, замыкание — функция, которая ссылается на свободные переменные в своём контексте.
****

Наверное, самый простой способ понять, что такое замыкание, это представить его в виде переменной, которая имеет супер-возможность - доступ к другим локальным перменным, объявленным в той же области видимости, что и само замыкание.


Давайте сразу же посмотрим пример на javascript'e
[source,javascript]
----
var setKeyPress = function(callback) {
    document.onkeypress = callback;
}

var initialize = function() {
    var black = false;
    # <1>
    document.onclick = function() {
        black = !black;
        document.body.style.backgroundColor = black ? "#000000" : "transparent";
    }

    var displayValOfBlack = function() {
        alert(black);
    }

    setKeyPress(displayValOfBlack);
};

initialize();
----

Функция <1>, присвоенная к полям-функциям `document.onclick`, и функция `displayValOfBlack` - функции-замыкания. Заметьте, что они обе имеют ссылки на булеву переменную `black`, но эта перменная инициализируется не в теле функции. Из-за того, что `black` является локальной переменной по отношению к той области видимости, где определена функция, мы можем получить доступ до нее.   


****
Замыкание, так же как и экземпляр объекта, есть способ представления функциональности и данных, связанных и упакованных вместе.
****

If you put this in an HTML page:

Click to change to black
Hit [enter] to see "true"
Click again, changes back to white
Hit [enter] to see "false"
This demonstrates that both have access to the same black, and can be used to store state without any wrapper object.

The call to setKeyPress is to demonstrate how a function can be passed just like any variable. The scope preserved in the closure is still the one where the function was defined.

Closures are commonly used as event handlers, especially in JavaScript and ActionScript. Good use of closures will help you implicitly bind variables to event handlers without having to create an object wrapper. However, careless use will lead to memory leaks (such as when an unused but preserved event handler is the only thing to hold on to large objects in memory, especially DOM objects, preventing garbage collection).

****
Замыкание — это особый вид функции. Она определена в теле другой функции и создаётся каждый раз во время её выполнения. Синтакстически это выглядит как функция, находящаяся целиком в теле другой функции. При этом вложенная внутренняя функция содержит ссылки на локальные переменные внешней функции. Каждый раз при выполнении внешней функции происходит создание нового экземпляра внутренней функции, с новыми ссылками на переменные внешней функции.
****