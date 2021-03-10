FROM grandchef/php:7.4.15-fpm-alpine

RUN touch /var/log/cron.log && \
    apk add --no-cache \
    g++ \
    make \
    autoconf \
    bash \
    && pecl install xdebug \
    && docker-php-ext-enable xdebug \
    && docker-php-source delete \
    && apk del \
    g++ \
    make \
    autoconf \
    && rm -rf /var/cache/apk/*
