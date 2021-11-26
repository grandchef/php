FROM php:7.4.26-fpm-alpine

LABEL maintainer="Equipe grandChef <desenvolvimento@grandchef.com.br>"

RUN apk add --no-cache \
    wget \
    unzip \
    autoconf \
    g++ \
    make \
    libtool \
    pcre-dev \
    imagemagick \
    imagemagick-dev \
    bzip2 \
    bzip2-dev \
    freetype-dev \
    libjpeg-turbo-dev \
    libpng \
    libpng-dev \
    libzip \
    libzip-dev \
    libpq \
    postgresql-dev \
    && docker-php-ext-configure gd \
    --with-freetype \
    --with-jpeg \
    && docker-php-ext-install -j$(nproc) gd \
    && yes '' | pecl install imagick \
    && docker-php-ext-enable imagick \
    && pecl install redis \
    && docker-php-ext-enable redis \
    && docker-php-ext-install -j$(nproc) \
    zip \
    bz2 \
    opcache \
    pdo_pgsql \
    pdo_mysql \
    sockets \
    && docker-php-source delete \
    && apk del \
    autoconf \
    g++ \
    make \
    libtool \
    pcre-dev \
    bzip2-dev \
    freetype-dev \
    libjpeg-turbo-dev \
    libpng-dev \
    libzip-dev \
    postgresql-dev \
    imagemagick-dev \
    && rm -rf /var/cache/apk/*
