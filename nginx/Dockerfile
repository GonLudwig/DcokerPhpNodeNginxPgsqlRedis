FROM nginx:stable-alpine

ADD ./nginx/nginx.conf /etc/nginx/nginx.conf
ADD ./nginx/default.conf /etc/nginx/templates/default.conf.template

RUN mkdir -p /var/www/html/backend

RUN chown 1000:www-data /var/www/html/backend

RUN mkdir -p /var/www/html/frontend

RUN chown 1000:www-data /var/www/html/frontend