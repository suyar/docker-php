FROM centos:7

LABEL maintainer="su@zorzz.com"

RUN set -eux; \
    ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime; \
    curl -o /etc/yum.repos.d/CentOS-Base.repo http://mirrors.aliyun.com/repo/Centos-7.repo; \
    sed -i "/aliyuncs.com/d" /etc/yum.repos.d/CentOS-Base.repo; \
    curl -o /etc/yum.repos.d/epel.repo http://mirrors.aliyun.com/repo/epel-7.repo

RUN set -eux; \
    yum install -y \
    autoconf \
    make \
    gcc \
    gcc-c++ \
    libxml2-devel \
    readline-devel \
    bzip2-devel \
    zlib-devel \
    libmcrypt-devel \
    mhash-devel \
    openssl-devel \
    gdbm-devel \
    unixODBC-devel \
    gettext-devel \
    libicu-devel \
    libjpeg-turbo-devel \
    libpng-devel \
    freetype-devel \
    libXpm-devel \
    uw-imap-devel \
    gmp-devel \
    curl-devel \
    openldap-devel \
    libxslt-devel; \
    yum clean all

ENV PHP_VERSION=5.3.29 \
    PHP_INI_DIR=/usr/local/etc/php \
    PHP_INI_SCAN_DIR=/usr/local/etc/php/conf.d \
    PHP_FPM_DIR=/usr/local/etc \
    PHP_FPM_SCAN_DIR=/usr/local/etc/php-fpm.d

RUN set -eux; \
    mkdir -p ${PHP_INI_SCAN_DIR}; \
    mkdir -p ${PHP_FPM_SCAN_DIR}; \
    mkdir -p /var/www; \
    chmod 777 /var/www

RUN set -eux; \
    cd ~ \
    && curl -O https://www.php.net/distributions/php-${PHP_VERSION}.tar.gz \
    && tar -zxf php-${PHP_VERSION}.tar.gz \
    && cd php-${PHP_VERSION} \
    && ./configure \
    --with-libdir=lib64 \
    --with-config-file-path=${PHP_INI_DIR} \
    --with-config-file-scan-dir=${PHP_INI_SCAN_DIR} \
    --disable-cgi \
    --enable-fpm \
    --with-fpm-user=root \
    --with-fpm-group=root \
    --with-readline \
    --with-bz2 \
    --enable-zip \
    --with-zlib \
    --with-mcrypt \
    --with-mhash \
    --with-openssl \
    --enable-dba \
    --with-gdbm \
    --with-unixODBC=/usr \
    --enable-inifile \
    --with-pdo-mysql=mysqlnd \
    --with-pdo-odbc=unixODBC,/usr \
    --with-mysqli=mysqlnd \
    --with-mysql=mysqlnd \
    --enable-calendar \
    --with-gettext \
    --enable-intl \
    --enable-mbstring \
    --enable-exif \
    --with-gd \
    --with-jpeg-dir \
    --with-png-dir \
    --with-xpm-dir \
    --with-freetype-dir \
    --enable-gd-native-ttf \
    --with-imap \
    --with-imap-ssl \
    --with-kerberos \
    --enable-bcmath \
    --with-gmp \
    --enable-pcntl \
    --enable-sysvsem \
    --enable-sysvshm \
    --enable-sysvmsg \
    --enable-shmop \
    --with-curl \
    --enable-ftp \
    --with-ldap \
    --with-ldap-sasl \
    --enable-sockets \
    --with-regex \
    --enable-libxml \
    --enable-soap \
    --with-xmlrpc \
    --with-xsl \
    && sed -i '/^EXTRA_LIBS/s/$/ -lstdc++/' Makefile \
    && make -j $(nproc) \
    && make install \
    && make clean \
    && cp php.ini-production ${PHP_INI_DIR}/php.ini-production \
    && cp php.ini-development ${PHP_INI_DIR}/php.ini-development \
    && cp php.ini-development ${PHP_INI_DIR}/php.ini \
    && cp ${PHP_FPM_DIR}/php-fpm.conf.default ${PHP_FPM_DIR}/php-fpm.conf \
    && sed -i "s/^;include=.*/include=etc\/php-fpm.d\/*.conf/" ${PHP_FPM_DIR}/php-fpm.conf \
    && echo 'daemonize = no' > ${PHP_FPM_SCAN_DIR}/docker.conf \
    && pecl channel-update pecl.php.net \
    && cd ~ \
    && rm -rf php*

COPY docker-php-* /usr/local/bin/

RUN set -eux; \
    chmod +x /usr/local/bin/docker-php-*

RUN docker-php-install \
    amqp \
    apcu \
    gmagick \
    hrtime \
    igbinary \
    libsodium \
    lzf \
    memcache \
    memcached \
    mongo \
    mongodb \
    msgpack \
    oauth \
    rar \
    redis \
    solr \
    ssh2 \
    stomp \
    svm \
    swoole \
    sync \
    timezonedb \
    varnish \
    yaf \
    yaml \
    yar \
    opcache \
    zookeeper

ENTRYPOINT ["docker-php-entrypoint"]

WORKDIR /var/www

EXPOSE 9000

CMD ["php-fpm", "-R"]
