FROM ubuntu:16.04

COPY test.conf /etc/apache2/sites-available/

RUN apt-get update && \
    apt-get install vim apache2 libapache2-mod-php7.0 -y && \
    mkdir /var/www/html/test && \
    a2enmod rewrite && \
    a2ensite test.conf

WORKDIR /var/www/html/test

EXPOSE 80

CMD ["apachectl", "-D", "FOREGROUND"]
