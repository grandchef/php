FROM fpm-alpine

LABEL maintainer="Equipe grandChef <desenvolvimento@grandchef.com.br>"

RUN apk add --no-cache \
    bash \
    nginx \
    && mkdir -p /run/nginx \
    && rm -f  /etc/nginx/sites-enabled/default \
    && rm -f  /var/www/html/index.nginx-debian.html \
    && rm -rf  /var/www/localhost \
    && rm -rf /var/cache/apk/*
