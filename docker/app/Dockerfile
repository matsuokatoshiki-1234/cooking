FROM php:7.4.2-fpm-alpine3.11

COPY --from=composer:1.9.3 /usr/bin/composer /usr/bin/composer

RUN apk update \
    && apk add \
    libzip-dev \
    npm \
    && docker-php-ext-install \
    zip \
    pdo_mysql

WORKDIR /var/www/cooking