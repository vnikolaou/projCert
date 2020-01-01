FROM php:7.1.8-apache

MAINTAINER Evangelos Nikolaou
COPY . /srv/app/public
RUN rm -r /srv/app/public/docker
COPY ./docker/apache.conf /etc/apache2/sites-available/000-default.conf

RUN chown -R www-data:www-data /srv/app/public \
    && a2enmod rewrite
