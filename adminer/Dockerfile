FROM adminer:latest
RUN apt-get update \
 && apt-get install -y freetds-dev libsybdb5 php8.0-sybase \
 && docker-php-ext-install pdo_dblib \
 && rm -rf /var/lib/apt/lists/*
