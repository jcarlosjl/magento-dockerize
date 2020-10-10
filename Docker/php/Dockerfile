FROM php:7.4-fpm
RUN apt-get update && \
    apt-get install -y \
    zlib1g-dev libpng-dev libjpeg62-turbo-dev libjpeg-dev libicu-dev \
    libxml2-dev libxslt1-dev libzip-dev libfreetype6-dev

RUN docker-php-ext-install pdo_mysql
RUN docker-php-ext-install zip
RUN docker-php-ext-configure gd --with-freetype --with-jpeg
RUN docker-php-ext-install -j "$(nproc)" gd
RUN docker-php-ext-install bcmath
RUN docker-php-ext-install intl
RUN docker-php-ext-install soap
RUN docker-php-ext-install xsl
RUN docker-php-ext-install zip
RUN docker-php-ext-install sockets