FROM nginx:stable-alpine

ADD ./nginx/nginx.conf /etc/nginx/nginx.conf
ADD ./nginx/default.conf /etc/nginx/templates/default.conf.template

RUN mkdir -p /var/www/html

RUN chown 1000:www-data /var/www/html