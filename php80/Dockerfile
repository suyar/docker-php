FROM centos:8

LABEL maintainer="su@zorzz.com"

RUN ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime

RUN set -eux; \
    dnf install -y epel-release; \
    dnf --enablerepo=powertools install -y \
    autoconf \
    make \
    gcc \
    gcc-c++ \
    libxml2-devel \
    readline-devel \
    bzip2-devel \
    zlib-devel \
    libzip-devel \
    mhash-devel \
    openssl-devel \
    libsodium-devel \
    sqlite-devel \
    libpq-devel \
    gettext-devel \
    libicu-devel \
    libwebp-devel \
    libjpeg-turbo-devel \
    freetype-devel \
    oniguruma-devel \
    libXpm-devel \
    gmp-devel \
    curl-devel \
    libxslt-devel \
    libtidy-devel; \
    dnf clean all

ENV PHP_VERSION=8.0.9 \
    PHP_PREFIX=/usr/local/php \
    PHP_BIN_DIR=/usr/local/bin \
    PHP_SBIN_DIR=/usr/local/sbin \
    PHP_INI_DIR=/usr/local/php/etc \
    PHP_INI_SCAN_DIR=/usr/local/php/etc/conf.d \
    PHP_FPM_DIR=/usr/local/php/etc \
    PHP_FPM_SCAN_DIR=/usr/local/php/etc/php-fpm.d \
    PHP_EXT_DIR=/usr/local/php/ext

RUN set -eux; \
    mkdir -p ${PHP_INI_SCAN_DIR}; \
    mkdir -p ${PHP_FPM_SCAN_DIR}; \
    mkdir -p ${PHP_EXT_DIR}

RUN set -eux; \
    cd ~; \
    curl -O https://www.php.net/distributions/php-${PHP_VERSION}.tar.gz; \
    tar -zxf php-${PHP_VERSION}.tar.gz; \
    cd php-${PHP_VERSION}; \
    ./configure \
    --with-libdir=lib64 \
    --prefix=${PHP_PREFIX} \
    --bindir=${PHP_BIN_DIR} \
    --sbindir=${PHP_SBIN_DIR} \
    --with-config-file-path=${PHP_INI_DIR} \
    --with-config-file-scan-dir=${PHP_INI_SCAN_DIR} \
    --disable-cgi \
    --enable-fpm \
    --enable-mysqlnd \
    --with-readline \
    --with-bz2 \
    --with-zip \
    --with-zlib \
    --with-mhash \
    --with-openssl \
    --with-sodium \
    --with-pdo-mysql=mysqlnd \
    --with-pdo-pgsql \
    --with-mysqli=mysqlnd \
    --with-pgsql \
    --enable-calendar \
    --with-gettext \
    --enable-intl \
    --enable-mbstring \
    --enable-exif \
    --enable-gd \
    --with-webp \
    --with-jpeg \
    --with-xpm \
    --with-freetype \
    --enable-bcmath \
    --with-gmp \
    --enable-pcntl \
    --with-curl \
    --enable-ftp \
    --enable-sockets \
    --with-xsl \
    --with-tidy \
    --with-pear; \
    make -j $(nproc); \
    make install; \
    make clean; \
    cp php.ini-production ${PHP_INI_DIR}/php.ini-production; \
    cp php.ini-development ${PHP_INI_DIR}/php.ini-development; \
    cp php.ini-development ${PHP_INI_DIR}/php.ini; \
    cp ${PHP_FPM_DIR}/php-fpm.conf.default ${PHP_FPM_DIR}/php-fpm.conf; \
    cp ${PHP_FPM_SCAN_DIR}/www.conf.default ${PHP_FPM_SCAN_DIR}/www.conf; \
    cd ~; \
    rm -rf php-*; \
    pecl update-channels

RUN set -eux; \
    { \
        echo '[www]'; \
        echo 'user = root'; \
        echo 'group = root'; \
    } | tee ${PHP_FPM_SCAN_DIR}/xx-docker.conf; \
    { \
        echo '[global]'; \
        echo 'daemonize = no'; \
        echo; \
        echo '[www]'; \
        echo 'listen = 9000'; \
    } | tee ${PHP_FPM_SCAN_DIR}/zz-docker.conf

COPY docker-php-* /usr/local/bin/
RUN chmod +x /usr/local/bin/docker-php-*

ARG PHP_EXTENSIONS="amqp apcu igbinary lzf memcached mongodb msgpack redis swoole xlswriter yaml opcache"
RUN docker-php-install ${PHP_EXTENSIONS}

RUN set -eux; \
    cd ~; \
    php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"; \
    php composer-setup.php --install-dir=/usr/local/bin --filename=composer; \
    php -r "unlink('composer-setup.php');"; \
    chmod +x /usr/local/bin/composer

ENTRYPOINT ["docker-php-entrypoint"]
WORKDIR /var/www

STOPSIGNAL SIGQUIT

EXPOSE 9000
CMD ["php-fpm", "-R"]
