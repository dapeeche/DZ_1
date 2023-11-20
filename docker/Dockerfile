FROM php:8.2-apache

RUN docker-php-ext-install -j$(nproc) pdo_mysql

RUN apt-get update && apt-get upgrade -y && apt-get install -y git && docker-php-ext-install pdo_mysql && apt-get install libpq-dev -y

COPY default.conf /etc/apache2/sites-available/000-default.conf