FROM php:7.4.1-fpm-alpine3.10
RUN docker-php-ext-install mysqli pdo pdo_mysql
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer
WORKDIR /var/www/html