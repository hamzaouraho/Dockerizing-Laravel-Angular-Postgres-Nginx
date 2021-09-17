# FROM php:8.0.3-fpm-alpine3.12

# RUN docker-php-ext-install pdo pdo_mysql

# RUN apk add libzip-dev

# RUN docker-php-ext-install zip

# RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
# FROM php:8.0-fpm-alpine

# RUN php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');" \
#     && php composer-setup.php --install-dir=/usr/local/bin --filename=composer \
#     && php -r "unlink('composer-setup.php');" \
#     && docker-php-ext-install mysqli pdo_mysql

# RUN mv "$PHP_INI_DIR/php.ini-production" "$PHP_INI_DIR/php.ini"
# RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# RUN set -ex \
#     	&& apk --no-cache add postgresql-dev nodejs yarn npm\
#     	&& docker-php-ext-install pdo pdo_pgsql
# WORKDIR /var/www/html

# FROM php:8.0.3-fpm-alpine3.12

# RUN docker-php-ext-install pdo pdo_mysql

# RUN apk add libzip-dev

# RUN docker-php-ext-install zip

# RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# FROM php:7.3-fpm-alpine

# RUN apk update; \
#     apk upgrade;

# RUN set -ex \
#   && apk --no-cache add \
#     postgresql-dev

# RUN docker-php-ext-install pdo pdo_pgsql

# COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

# RUN adduser --uid 1001 --disabled-password --home /home/devuser devuser
# RUN mkdir -p /home/devuser/.composer && \
#     chown -R devuser:devuser /home/devuser
# RUN addgroup devuser www-data
# RUN addgroup devuser root

# RUN chgrp -R  www-data /var/www/html
# RUN chmod -R g+r /var/www/html/

# RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
FROM php:8.0-fpm-alpine

RUN php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');" \
    && php composer-setup.php --install-dir=/usr/local/bin --filename=composer \
    && php -r "unlink('composer-setup.php');" \
    && docker-php-ext-install mysqli pdo_mysql

RUN mv "$PHP_INI_DIR/php.ini-production" "$PHP_INI_DIR/php.ini"
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

RUN set -ex \
    	&& apk --no-cache add postgresql-dev nodejs yarn npm\
    	&& docker-php-ext-install pdo pdo_pgsql
WORKDIR /var/www/html
