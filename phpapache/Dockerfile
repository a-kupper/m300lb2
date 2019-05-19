FROM php:7.2-apache-stretch



# install and activate apache extensions
RUN apt-get update -y \
    && apt-get install -y libjpeg62-turbo-dev libfreetype6-dev libpng-dev libgmp-dev libxml2-dev \
    && docker-php-ext-configure gd --with-freetype-dir --with-jpeg-dir \
    && docker-php-ext-install -j$(nproc) opcache mysqli pdo pdo_mysql gd exif zip gmp soap
RUN a2enmod rewrite expires ssl headers


# install ssmtp (mail)
RUN apt-get install -y ssmtp
COPY ./ssmtp.conf /etc/ssmtp/

# --- install other tools ---
WORKDIR /root


# change document root
ENV APACHE_DOCUMENT_ROOT /var/www/httpdocs
RUN sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf
RUN sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf


# configure php
COPY ./php.ini /usr/local/etc/php/

# configure apache
COPY localhost.crt /etc/apache2/ssl/server.crt
COPY localhost.key /etc/apache2/ssl/server.key
COPY localhost_secure.conf /etc/apache2/sites-enabled/dev.conf
COPY 000-default.conf /etc/apache2/sites-available/000-default.conf

#trust certificate 
COPY localhost.crt /usr/local/share/ca-certificates/localhost.crt
RUN update-ca-certificates


# start server
CMD ["apache2-foreground"]
