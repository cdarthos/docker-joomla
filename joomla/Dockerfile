# Dockerfile
# syntax=docker/dockerfile:1

# Dockerfile
FROM php:8.0-apache

WORKDIR /app

RUN apt-get update && apt-get install -y \
    zlib1g-dev \
    libzip-dev \
    libpng-dev \
    libicu-dev

# Parametre d apache
COPY conf/vhost.conf /etc/apache2/sites-available/000-default.conf
COPY conf/apache.conf /etc/apache2/conf-available/z-app.conf
COPY conf/php.ini /usr/local/etc/php/conf.d/app.ini
RUN a2enconf z-app

RUN docker-php-ext-configure zip && docker-php-ext-install mysqli zip gd intl && docker-php-ext-enable mysqli zip gd intl

COPY ./app /app




