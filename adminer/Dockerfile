FROM adminer:latest

USER root

# Instala dependencias de compilación y FreeTDS
RUN apk update && apk add --no-cache \
      freetds-dev \
      unixodbc-dev \
      build-base \
      autoconf \
      libtool \
    \
    # Compila e instala pdo_dblib
    && docker-php-ext-install pdo_dblib \
    \
    # Limpia dependencias de build
    && apk del build-base autoconf libtool \
    && rm -rf /var/cache/apk/*

USER www-data
