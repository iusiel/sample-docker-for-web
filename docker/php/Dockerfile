FROM php:7.4.4-fpm-alpine
RUN docker-php-ext-install mysqli pdo_mysql
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer
WORKDIR /var/www/html