FROM php:fpm-alpine3.18

ENV COMPOSER_ALLOW_SUPERUSER=1

COPY --from=composer:2.6.5 /usr/bin/composer /usr/bin/composer

COPY ./composer.* ./

RUN composer install --prefer-dist --no-dev --no-scripts --no-progress --no-interaction

RUN composer dump-autoload --optimize

