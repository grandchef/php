FROM composer:2.0.8

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
    && docker-php-ext-install -j$(nproc) \
    bcmath \
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
