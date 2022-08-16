FROM nginx:stable-alpine

ADD ./nginx/nginx.conf /etc/nginx/nginx.conf

ADD ./nginx/frontend.com.br.conf /etc/nginx/templates/frontend.com.br.conf.template

ADD ./nginx/backend.com.br.conf /etc/nginx/templates/backend.com.br.conf.template

RUN mkdir -p /var/www/html/backend

RUN mkdir -p /var/www/html/frontend

RUN addgroup -g 1000 laravel && adduser -G laravel -g laravel -s /bin/sh -D laravel

RUN chown -R laravel:laravel /var/www/html