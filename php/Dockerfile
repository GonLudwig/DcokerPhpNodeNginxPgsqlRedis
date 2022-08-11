FROM php:8.1-fpm-alpine

ADD ./php/www.conf /usr/local/etc/php-fpm.d/www.conf

ADD ./php/php.ini /usr/local/etc/php/conf.d/php.ini

RUN addgroup -g 1000 laravel && adduser -G laravel -g laravel -s /bin/sh -D laravel

RUN mkdir -p /var/www/html/backend

RUN chown laravel:laravel /var/www/html

WORKDIR /var/www/html/backend

RUN apk add --no-cache \
    freetype \
    libpng \
    libpq-dev \
    libjpeg-turbo \
    freetype-dev \
    libpng-dev \
    libjpeg-turbo-dev \
    postgresql-dev

RUN docker-php-ext-configure gd \
    --with-freetype \
    --with-jpeg

RUN docker-php-ext-install pdo pdo_pgsql pgsql