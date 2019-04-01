FROM php:7-apache

RUN openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/ssl/private/ssl-cert-snakeoil.key -out /etc/ssl/certs/ssl-cert-snakeoil.pem -subj "/C=BR/ST=Rio Grande do Sul/L=Porto Alegre/O=Security/OU=Development/CN=example.com"

RUN a2enmod rewrite
RUN a2ensite default-ssl
RUN a2enmod ssl

EXPOSE 443

COPY ./html /var/www/html
COPY ./html /var/www/html

WORKDIR /var/www/html