# Utiliser l'image de base PHP 7.4 CLI
FROM php:7.4-cli

# Installer les dépendances nécessaires et les extensions PHP
RUN apt-get update && \
    apt-get install -y libzip-dev libicu-dev libonig-dev libfreetype-dev libjpeg62-turbo-dev libpng-dev && \
    docker-php-ext-configure gd --with-freetype --with-jpeg && \
    docker-php-ext-install zip intl gd pdo_mysql opcache

RUN mv "$PHP_INI_DIR/php.ini-development" "$PHP_INI_DIR/php.ini"
