FROM php:8.1-fpm-alpine3.15

COPY --from=composer:2.2 /usr/bin/composer /usr/local/bin/composer
COPY --from=mlocati/php-extension-installer /usr/bin/install-php-extensions /usr/local/bin/

RUN install-php-extensions xdebug-stable gd exif

WORKDIR /var/www/mini-framework
