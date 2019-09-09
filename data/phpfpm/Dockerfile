FROM php:7.2-fpm-alpine
RUN set -x && \
  apk add --no-cache icu-libs && \
  apk add --no-cache libzip && \
  apk add --no-cache libzip-dev && \
  apk add --no-cache php7-zlib && \
  apk add --no-cache php7-zip && \
  apk add --no-cache php7-gd && \
  apk add --no-cache php7-xml && \
  apk add --no-cache libxml2 libxml2-dev && \
  apk add --no-cache libpng libpng-dev && \
  apk add --no-cache --virtual build-dependencies icu-dev && \
  NPROC=$(grep -c ^processor /proc/cpuinfo 2>/dev/null || 1) && \
  docker-php-ext-install -j${NPROC} intl && \
  docker-php-ext-install -j${NPROC} pdo_mysql && \
  docker-php-ext-install gd && \
  docker-php-ext-install zip && \
  docker-php-ext-install xml && \
  apk del --no-cache --purge build-dependencies && \
  rm -rf /tmp/pear
RUN set -x && \
  deluser www-data && \
  addgroup -g 50 -S www-data && \
  adduser -u 1000 -D -S -G www-data www-data
