
FROM php:apache

RUN apt-get update && \
    apt-get install -y wget libpng-dev libjpeg-dev libonig-dev libxml2-dev unzip && \
    docker-php-ext-install mysqli mbstring

WORKDIR /var/www/html

RUN wget https://github.com/poweradmin/poweradmin/archive/refs/tags/v3.4.1.tar.gz && \
    tar -xzf v3.4.1.tar.gz && \
    mv poweradmin-3.4.1/* . && \
    rm -rf poweradmin-3.4.1 v3.4.1.tar.gz

EXPOSE 8080
