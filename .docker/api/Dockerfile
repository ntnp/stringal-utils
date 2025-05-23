FROM ntnp/laravel-dev:8.3
USER root

# Add gd
RUN apt-get update; \
    apt-get install -y libfreetype-dev libjpeg62-turbo-dev libpng-dev

RUN docker-php-ext-configure gd --with-freetype --with-jpeg; \
    docker-php-ext-install -j$(nproc) gd; \
    docker-php-ext-enable gd

###

USER php
WORKDIR /var/www/html
