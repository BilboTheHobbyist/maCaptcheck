FROM php:7.2-apache

RUN docker-php-ext-install mysqli pdo pdo_mysql
RUN docker-php-ext-enable mysqli

RUN a2enmod rewrite

RUN apt-get update && apt-get install -y zlib1g-dev libpng-dev libfreetype6-dev

RUN docker-php-ext-configure gd --with-gd --with-zlib-dir --with-png-dir --with-freetype-dir

RUN docker-php-ext-install gd

