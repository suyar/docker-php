# Docker Images For PHP

[![docker pulls](https://img.shields.io/docker/pulls/suyar/php)](https://hub.docker.com/r/suyar/php)

## 仓库概述

基于官方镜像的 PHP 镜像，已安装常用扩展。

PHP 版本生命周期参考 [PHP 版本支持](https://www.php.net/supported-versions.php)

- 基于 [PHP Official Images](https://hub.docker.com/_/php)
- 基于 [docker-php-extension-installer](https://github.com/mlocati/docker-php-extension-installer)
- 基于 `GitHub Actions` 自动构建

## 构建镜像

### 主要镜像

这些镜像都是从官方镜像构建的，不包含其他第三方软件。

- PHP 7.0
    - [`suyar/php:7.0-fpm`](https://hub.docker.com/r/suyar/php/tags?name=7.0-fpm)
    - [`suyar/php:7.0-fpm-alpine`](https://hub.docker.com/r/suyar/php/tags?name=7.0-fpm-alpine)
    - [`suyar/php:7.0-cli`](https://hub.docker.com/r/suyar/php/tags?name=7.0-cli)
    - [`suyar/php:7.0-cli-alpine`](https://hub.docker.com/r/suyar/php/tags?name=7.0-cli-alpine)
- PHP 7.1
    - [`suyar/php:7.1-fpm`](https://hub.docker.com/r/suyar/php/tags?name=7.1-fpm)
    - [`suyar/php:7.1-fpm-alpine`](https://hub.docker.com/r/suyar/php/tags?name=7.1-fpm-alpine)
    - [`suyar/php:7.1-cli`](https://hub.docker.com/r/suyar/php/tags?name=7.1-cli)
    - [`suyar/php:7.1-cli-alpine`](https://hub.docker.com/r/suyar/php/tags?name=7.1-cli-alpine)
- PHP 7.2
    - [`suyar/php:7.2-fpm`](https://hub.docker.com/r/suyar/php/tags?name=7.2-fpm)
    - [`suyar/php:7.2-fpm-alpine`](https://hub.docker.com/r/suyar/php/tags?name=7.2-fpm-alpine)
    - [`suyar/php:7.2-cli`](https://hub.docker.com/r/suyar/php/tags?name=7.2-cli)
    - [`suyar/php:7.2-cli-alpine`](https://hub.docker.com/r/suyar/php/tags?name=7.2-cli-alpine)
- PHP 7.3
    - [`suyar/php:7.3-fpm`](https://hub.docker.com/r/suyar/php/tags?name=7.3-fpm)
    - [`suyar/php:7.3-fpm-alpine`](https://hub.docker.com/r/suyar/php/tags?name=7.3-fpm-alpine)
    - [`suyar/php:7.3-cli`](https://hub.docker.com/r/suyar/php/tags?name=7.3-cli)
    - [`suyar/php:7.3-cli-alpine`](https://hub.docker.com/r/suyar/php/tags?name=7.3-cli-alpine)
- PHP 7.4
    - [`suyar/php:7.4-fpm`](https://hub.docker.com/r/suyar/php/tags?name=7.4-fpm)
    - [`suyar/php:7.4-fpm-alpine`](https://hub.docker.com/r/suyar/php/tags?name=7.4-fpm-alpine)
    - [`suyar/php:7.4-cli`](https://hub.docker.com/r/suyar/php/tags?name=7.4-cli)
    - [`suyar/php:7.4-cli-alpine`](https://hub.docker.com/r/suyar/php/tags?name=7.4-cli-alpine)
- PHP 8.0
    - [`suyar/php:8.0-fpm`](https://hub.docker.com/r/suyar/php/tags?name=8.0-fpm)
    - [`suyar/php:8.0-fpm-alpine`](https://hub.docker.com/r/suyar/php/tags?name=8.0-fpm-alpine)
    - [`suyar/php:8.0-cli`](https://hub.docker.com/r/suyar/php/tags?name=8.0-cli)
    - [`suyar/php:8.0-cli-alpine`](https://hub.docker.com/r/suyar/php/tags?name=8.0-cli-alpine)
- PHP 8.1
    - [`suyar/php:8.1-fpm`](https://hub.docker.com/r/suyar/php/tags?name=8.1-fpm)
    - [`suyar/php:8.1-fpm-alpine`](https://hub.docker.com/r/suyar/php/tags?name=8.1-fpm-alpine)
    - [`suyar/php:8.1-cli`](https://hub.docker.com/r/suyar/php/tags?name=8.1-cli)
    - [`suyar/php:8.1-cli-alpine`](https://hub.docker.com/r/suyar/php/tags?name=8.1-cli-alpine)
- PHP 8.2
    - [`suyar/php:8.2-fpm`](https://hub.docker.com/r/suyar/php/tags?name=8.2-fpm)
    - [`suyar/php:8.2-fpm-alpine`](https://hub.docker.com/r/suyar/php/tags?name=8.2-fpm-alpine)
    - [`suyar/php:8.2-cli`](https://hub.docker.com/r/suyar/php/tags?name=8.2-cli)
    - [`suyar/php:8.2-cli-alpine`](https://hub.docker.com/r/suyar/php/tags?name=8.2-cli-alpine)

### 辅助镜像

这些镜像都是从『主要镜像』构建的，包含 `supervisor` 或 `cron`。

- PHP 7.0
    - [`suyar/php:7.0-cli-supervisor`](https://hub.docker.com/r/suyar/php/tags?name=7.0-cli-supervisor)
    - [`suyar/php:7.0-cli-alpine-supervisor`](https://hub.docker.com/r/suyar/php/tags?name=7.0-cli-alpine-supervisor)
    - [`suyar/php:7.0-cli-cron`](https://hub.docker.com/r/suyar/php/tags?name=7.0-cli-cron)
    - [`suyar/php:7.0-cli-alpine-cron`](https://hub.docker.com/r/suyar/php/tags?name=7.0-cli-alpine-cron)
- PHP 7.1
    - [`suyar/php:7.1-cli-supervisor`](https://hub.docker.com/r/suyar/php/tags?name=7.1-cli-supervisor)
    - [`suyar/php:7.1-cli-alpine-supervisor`](https://hub.docker.com/r/suyar/php/tags?name=7.1-cli-alpine-supervisor)
    - [`suyar/php:7.1-cli-cron`](https://hub.docker.com/r/suyar/php/tags?name=7.1-cli-cron)
    - [`suyar/php:7.1-cli-alpine-cron`](https://hub.docker.com/r/suyar/php/tags?name=7.1-cli-alpine-cron)
- PHP 7.2
    - [`suyar/php:7.2-cli-supervisor`](https://hub.docker.com/r/suyar/php/tags?name=7.2-cli-supervisor)
    - [`suyar/php:7.2-cli-alpine-supervisor`](https://hub.docker.com/r/suyar/php/tags?name=7.2-cli-alpine-supervisor)
    - [`suyar/php:7.2-cli-cron`](https://hub.docker.com/r/suyar/php/tags?name=7.2-cli-cron)
    - [`suyar/php:7.2-cli-alpine-cron`](https://hub.docker.com/r/suyar/php/tags?name=7.2-cli-alpine-cron)
- PHP 7.3
    - [`suyar/php:7.3-cli-supervisor`](https://hub.docker.com/r/suyar/php/tags?name=7.3-cli-supervisor)
    - [`suyar/php:7.3-cli-alpine-supervisor`](https://hub.docker.com/r/suyar/php/tags?name=7.3-cli-alpine-supervisor)
    - [`suyar/php:7.3-cli-cron`](https://hub.docker.com/r/suyar/php/tags?name=7.3-cli-cron)
    - [`suyar/php:7.3-cli-alpine-cron`](https://hub.docker.com/r/suyar/php/tags?name=7.3-cli-alpine-cron)
- PHP 7.4
    - [`suyar/php:7.4-cli-supervisor`](https://hub.docker.com/r/suyar/php/tags?name=7.4-cli-supervisor)
    - [`suyar/php:7.4-cli-alpine-supervisor`](https://hub.docker.com/r/suyar/php/tags?name=7.4-cli-alpine-supervisor)
    - [`suyar/php:7.4-cli-cron`](https://hub.docker.com/r/suyar/php/tags?name=7.4-cli-cron)
    - [`suyar/php:7.4-cli-alpine-cron`](https://hub.docker.com/r/suyar/php/tags?name=7.4-cli-alpine-cron)
- PHP 8.0
    - [`suyar/php:8.0-cli-supervisor`](https://hub.docker.com/r/suyar/php/tags?name=8.0-cli-supervisor)
    - [`suyar/php:8.0-cli-alpine-supervisor`](https://hub.docker.com/r/suyar/php/tags?name=8.0-cli-alpine-supervisor)
    - [`suyar/php:8.0-cli-cron`](https://hub.docker.com/r/suyar/php/tags?name=8.0-cli-cron)
    - [`suyar/php:8.0-cli-alpine-cron`](https://hub.docker.com/r/suyar/php/tags?name=8.0-cli-alpine-cron)
- PHP 8.1
    - [`suyar/php:8.1-cli-supervisor`](https://hub.docker.com/r/suyar/php/tags?name=8.1-cli-supervisor)
    - [`suyar/php:8.1-cli-alpine-supervisor`](https://hub.docker.com/r/suyar/php/tags?name=8.1-cli-alpine-supervisor)
    - [`suyar/php:8.1-cli-cron`](https://hub.docker.com/r/suyar/php/tags?name=8.1-cli-cron)
    - [`suyar/php:8.1-cli-alpine-cron`](https://hub.docker.com/r/suyar/php/tags?name=8.1-cli-alpine-cron)
- PHP 8.2
    - [`suyar/php:8.2-cli-supervisor`](https://hub.docker.com/r/suyar/php/tags?name=8.2-cli-supervisor)
    - [`suyar/php:8.2-cli-alpine-supervisor`](https://hub.docker.com/r/suyar/php/tags?name=8.2-cli-alpine-supervisor)
    - [`suyar/php:8.2-cli-cron`](https://hub.docker.com/r/suyar/php/tags?name=8.2-cli-cron)
    - [`suyar/php:8.2-cli-alpine-cron`](https://hub.docker.com/r/suyar/php/tags?name=8.2-cli-alpine-cron)

## 集成镜像

这些镜像都是从『主要镜像』构建的，包含 `composer`、`php-fpm`、`supervisor` 和 `cron`，其中 `php-fpm` 和 `cron` 使用 `supervisor` 管理。

- PHP 7.0
    - [`suyar/php:7.0-integration`](https://hub.docker.com/r/suyar/php/tags?name=7.0-integration)
    - [`suyar/php:7.0-alpine-integration`](https://hub.docker.com/r/suyar/php/tags?name=7.0-alpine-integration)
- PHP 7.1
    - [`suyar/php:7.1-integration`](https://hub.docker.com/r/suyar/php/tags?name=7.1-integration)
    - [`suyar/php:7.1-alpine-integration`](https://hub.docker.com/r/suyar/php/tags?name=7.1-alpine-integration)
- PHP 7.2
    - [`suyar/php:7.2-integration`](https://hub.docker.com/r/suyar/php/tags?name=7.2-integration)
    - [`suyar/php:7.2-alpine-integration`](https://hub.docker.com/r/suyar/php/tags?name=7.2-alpine-integration)
- PHP 7.3
    - [`suyar/php:7.3-integration`](https://hub.docker.com/r/suyar/php/tags?name=7.3-integration)
    - [`suyar/php:7.3-alpine-integration`](https://hub.docker.com/r/suyar/php/tags?name=7.3-alpine-integration)
- PHP 7.4
    - [`suyar/php:7.4-integration`](https://hub.docker.com/r/suyar/php/tags?name=7.4-integration)
    - [`suyar/php:7.4-alpine-integration`](https://hub.docker.com/r/suyar/php/tags?name=7.4-alpine-integration)
- PHP 8.0
    - [`suyar/php:8.0-integration`](https://hub.docker.com/r/suyar/php/tags?name=8.0-integration)
    - [`suyar/php:8.0-alpine-integration`](https://hub.docker.com/r/suyar/php/tags?name=8.0-alpine-integration)
- PHP 8.1
    - [`suyar/php:8.1-integration`](https://hub.docker.com/r/suyar/php/tags?name=8.1-integration)
    - [`suyar/php:8.1-alpine-integration`](https://hub.docker.com/r/suyar/php/tags?name=8.1-alpine-integration)
- PHP 8.2
    - [`suyar/php:8.2-integration`](https://hub.docker.com/r/suyar/php/tags?name=8.2-integration)
    - [`suyar/php:8.2-alpine-integration`](https://hub.docker.com/r/suyar/php/tags?name=8.2-alpine-integration)

## 使用镜像

```
docker pull suyar/php:8.2-fpm
```

镜像仓库 [https://hub.docker.com/r/suyar/php](https://hub.docker.com/r/suyar/php)

更多用法请参考 [PHP 官方镜像](https://hub.docker.com/_/php)

## 预装扩展

预装扩展请以对应镜像的 `Dockerfile` 文件为准。

```
docker run --rm suyar/php:8.2-cli php -m

[PHP Modules]
amqp
apcu
bcmath
bz2
calendar
Core
ctype
curl
date
decimal
dom
enchant
event
exif
fileinfo
filter
ftp
gd
gettext
gmp
hash
iconv
igbinary
imagick
intl
json
libxml
lzf
mbstring
memcached
mongodb
msgpack
mysqli
mysqlnd
openssl
pcntl
pcre
PDO
pdo_mysql
pdo_pgsql
pdo_sqlite
pgsql
Phar
posix
random
readline
redis
Reflection
session
SimpleXML
sockets
sodium
SPL
sqlite3
standard
swoole
tidy
timezonedb
tokenizer
uuid
xlswriter
xml
xmlreader
xmlwriter
xsl
yac
yaml
Zend OPcache
zip
zlib

[Zend Modules]
Zend OPcache
```
