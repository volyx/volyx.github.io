---
author: "volyx"
title:  "Сборка Nginx с модулями"
date: "2015-01-26"
# description: "Sample article showcasing basic Markdown syntax and formatting for HTML elements."
tags:  ["old-posts"]
categories: ["old-posts"]
summary: "by Brian Goetz, Tim Peierls, Joshua Bloch, Joseph Bowbeer, David Holmes, Doug Lea. I was fortunate indeed to have worked with a fantastic team on the design and implementation of the concurrency features added to the Java platform in Java 5.0 and Java 6. Now this same team provides the best explanation yet of these new features, and of concurrency in general. Concurrency is no longer a subject for advanced users only. Every Java developer should read this book. --Martin Buchholz"
image: "../img/nginx_with_modules.jpg"
# series: ["Themes Guide"]
# aliases: ["migrate-from-jekyl"]
# ShowToc: true
# TocOpen: true
# weight: 2
---


Сборка Nginx с модулями nginx-upload-module nginx-rtmp-module

Для начало скачиваем последнюю стабильную версию nginx:

wget http://nginx.org/download/nginx-1.4.6.tar.gz
tar xzf nginx-1.4.6.tar.gz
Далее с github скачиваем нужные нам модули:

git clone https://github.com/yaoweibin/nginx_cross_origin_module.git
git clone https://github.com/arut/nginx-rtmp-module.git
git clone -b 2.2 git://github.com/vkholodkov/nginx-upload-module.git
git clone https://github.com/masterzen/nginx-upload-progress-module.git
Устонавливаем библиотеку libpcre3-dev:

 apt-get install libpcre3-dev
после:

cd nginx-1.4.6/
конфигурируем:

./configure --add-module=../nginx-upload-module --add-module=../nginx-upload-progress-module --add-module=../nginx_cross_origin_module --add-module=../nginx-rtmp-module --prefix=/etc/nginx/ --sbin-path=/usr/sbin/nginx --conf-path=/etc/nginx/nginx.conf --error-log-path=/var/log/nginx/error.log --http-log-path=/var/log/nginx/access.log --pid-path=/var/run/nginx.pid --lock-path=/var/run/nginx.lock --http-client-body-temp-path=/var/cache/nginx/client_temp --user=nginx --group=nginx --with-http_realip_module --with-http_addition_module --with-http_sub_module --with-http_mp4_module --with-http_gzip_static_module --with-http_random_index_module --with-http_secure_link_module --with-http_stub_status_module --with-file-aio
принеобходимости можно еще добавить доболнительные параметры!

make
make install

Проверяем что у нас получилось:
root@root:~# nginx -V
nginx version: nginx/1.4.6
built by gcc 4.7.2 (Debian 4.7.2-5)
TLS SNI support enabled
configure arguments: --add-module=../nginx-upload-module --add-module=../nginx-upload-progress-module --add-module=../nginx_cross_origin_module --add-module=../nginx-rtmp-module --prefix=/etc/nginx/ --sbin-path=/usr/sbin/nginx --conf-path=/etc/nginx/nginx.conf --error-log-path=/var/log/nginx/error.log --http-log-path=/var/log/nginx/access.log --pid-path=/var/run/nginx.pid --lock-path=/var/run/nginx.lock --http-client-body-temp-path=/var/cache/nginx/client_temp --user=nginx --group=nginx --with-http_realip_module --with-http_addition_module --with-http_sub_module --with-http_mp4_module --with-http_gzip_static_module --with-http_random_index_module --with-http_secure_link_module --with-http_stub_status_module --with-file-aio