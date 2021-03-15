FROM php:7.4-fpm

RUN apt-get update && apt-get install -y \
        libfreetype6-dev \
        libjpeg62-turbo-dev \
        libpng-dev

RUN docker-php-ext-configure gd --with-freetype --with-jpeg
RUN docker-php-ext-install -j$(nproc) gd
RUN docker-php-ext-enable gd
RUN docker-php-ext-install mysqli
RUN docker-php-ext-enable mysqli
RUN docker-php-ext-install pdo_mysql
RUN docker-php-ext-enable pdo_mysql