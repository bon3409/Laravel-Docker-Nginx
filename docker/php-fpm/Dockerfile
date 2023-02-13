FROM php:8.1-fpm

WORKDIR "/var/www/html"

# 安裝 vim
RUN apt update -y
RUN apt install vim -y 

# 安裝 bash，並且預設用 bash 開啟
RUN apt install bash
RUN ln -sf /bin/bash /bin/sh

# 安裝 php redis 套件
RUN pecl install redis && docker-php-ext-enable redis

# 安裝 mysql 套件
RUN docker-php-ext-install pdo pdo_mysql

# 安裝 xdebug
RUN pecl install xdebug \
    && docker-php-ext-enable xdebug