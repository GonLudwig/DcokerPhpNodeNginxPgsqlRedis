FROM php:8.1-fpm-alpine

RUN mkdir -p /var/www/html/backend

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

ADD ./app /var/www/html/backend

RUN chown 1000:www-data /var/www/html/backend/storage/logs/laravel.log