# vim: ft=dockerfile

FROM php:7-fpm

RUN apt-get update && \
    apt-get install -y ca-certificates git && \
    rm -rf /var/lib/apt/lists/* \
    rm -rf /var/cache/apt/*
COPY DOIRootCA2.crt /usr/local/share/ca-certificates/ 
RUN update-ca-certificates

COPY php/composer-install.sh /tmp
RUN chmod +x /tmp/composer-install.sh && \
    /tmp/composer-install.sh && \
    rm -f /tmp/composer-install.sh

# Use default production config
RUN mv "$PHP_INI_DIR/php.ini-production" "$PHP_INI_DIR/php.ini"

