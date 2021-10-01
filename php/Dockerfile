FROM php:8.0-fpm

# install composer
RUN curl -sS https://getcomposer.org/installer | \
  php -- --install-dir=/usr/bin/ --filename=composer

RUN apt-get update \
    && apt-get -y install \
        libpng-dev \
        libzip-dev \
        libpq-dev

RUN docker-php-ext-install \
    gd \
    zip \
    pdo \
    pdo_pgsql \
    pgsql \
    pdo_mysql
