FROM ubuntu:latest

RUN apt-get update && apt-get install -y vim \
    curl \
    git \
    php7.0-fpm \
    php7.0-curl \
    php7.0-mbstring \
    php7.0-dom \
    php7.0-mysql \
    php7.0-gd

RUN curl -sL https://deb.nodesource.com/setup_7.x | bash /dev/stdin
RUN apt-get install -y nodejs
RUN npm install -g rimraf webpack

RUN php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
RUN php composer-setup.php
RUN php -r "unlink('composer-setup.php');"
RUN mv composer.phar /usr/local/bin/composer

WORKDIR /var/www