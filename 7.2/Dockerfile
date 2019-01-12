FROM ubuntu:16.04

MAINTAINER Armando Meeuwenoord <armando@codingexperts.nl>

RUN apt-get install -y software-properties-common && \
    add-apt-repository ppa:ondrej/php && \
    apt-get -y update && \
    apt-get -y --no-install-recommends install curl wget ca-certificates nano zip unzip git && \
    apt-get -y install \
    php7.2-cli \
    php7.2-curl \
    php7.2-dev \
    php7.2-gd \
    php7.2-intl \
    php7.2-mysql \
    php7.2-mbstring \
    php7.2-xml \
    php7.2-xsl \
    php7.2-zip \
    php7.2-json \
    php7.2-soap \
    php7.2-bcmath \
    unzip \
    && apt-get clean \
    && rm -rf \
    /var/lib/apt/lists/* \
    /tmp/* \
    /var/tmp/* \
    /usr/share/man \
    /usr/share/doc \
    /usr/share/doc-base

RUN curl -LO https://getcomposer.org/composer.phar \
    && chmod +x ./composer.phar \
    && mv ./composer.phar /usr/local/bin/composer

CMD ["/bin/bash"]
