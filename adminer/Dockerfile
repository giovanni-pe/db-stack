FROM adminer:latest

USER root

RUN apk update \
 && apk add --no-cache \
    freetds \
    freetds-dev \
    unixodbc-dev \
    php8-pdo_dblib \
 && rm -rf /var/cache/apk/*

USER www-data
