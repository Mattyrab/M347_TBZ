FROM php:8.0-apache
WORKDIR /var/www
COPY ./db.php ./info.php ./html/

RUN docker-php-ext-install mysqli

EXPOSE 80/tcp
EXPOSE 80/udp