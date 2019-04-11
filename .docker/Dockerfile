FROM    php:7.2-apache

LABEL   maintainer="Frederick Tyteca"

# setting apache user
ENV     APACHE_RUN_USER=www-data
ENV     APACHE_RUN_GROUP=www-data

# enabling mod rewrite
RUN     a2enmod rewrite

# setting timezone
ENV     TZ=Europe/Paris
RUN     ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

# default vhost replaced by custom one
# mainly documentRoot /srv/app
COPY    .docker/vhost.conf /etc/apache2/sites-available/000-default.conf

COPY    data/ /srv/app/

WORKDIR /srv/app