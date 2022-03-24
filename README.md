# Docker Images For PHP

## 仓库概述

基于官方镜像的 PHP 镜像，已安装常用扩展。

> 官方 PHP 版本生命周期参考 [PHP 版本支持](https://www.php.net/supported-versions.php)

- 基于 [PHP 官方镜像](https://hub.docker.com/_/php)
- 基于 [扩展安装工具](https://github.com/mlocati/docker-php-extension-installer)
- 基于 `GitHub Actions` 每周自动构建

## 构建镜像

### 主要镜像

这些镜像都是从官方镜像构建的，不包含其他第三方软件。

- suyar/php:7.0-fpm
- suyar/php:7.0-fpm-alpine
- suyar/php:7.0-cli
- suyar/php:7.0-cli-alpine
- suyar/php:7.1-fpm
- suyar/php:7.1-fpm-alpine
- suyar/php:7.1-cli
- suyar/php:7.1-cli-alpine
- suyar/php:7.2-fpm
- suyar/php:7.2-fpm-alpine
- suyar/php:7.2-cli
- suyar/php:7.2-cli-alpine
- suyar/php:7.3-fpm
- suyar/php:7.3-fpm-alpine
- suyar/php:7.3-cli
- suyar/php:7.3-cli-alpine
- suyar/php:7.4-fpm
- suyar/php:7.4-fpm-alpine
- suyar/php:7.4-cli
- suyar/php:7.4-cli-alpine
- suyar/php:8.0-fpm
- suyar/php:8.0-fpm-alpine
- suyar/php:8.0-cli
- suyar/php:8.0-cli-alpine
- suyar/php:8.1-fpm
- suyar/php:8.1-fpm-alpine
- suyar/php:8.1-cli
- suyar/php:8.1-cli-alpine

### 辅助镜像

这些镜像都是从『主要镜像』构建的，包含 `supervisor` 或 `cron`。

- suyar/php:7.0-cli-supervisor
- suyar/php:7.0-cli-alpine-supervisor
- suyar/php:7.0-cli-cron
- suyar/php:7.0-cli-alpine-cron
- suyar/php:7.1-cli-supervisor
- suyar/php:7.1-cli-alpine-supervisor
- suyar/php:7.1-cli-cron
- suyar/php:7.1-cli-alpine-cron
- suyar/php:7.2-cli-supervisor
- suyar/php:7.2-cli-alpine-supervisor
- suyar/php:7.2-cli-cron
- suyar/php:7.2-cli-alpine-cron
- suyar/php:7.3-cli-supervisor
- suyar/php:7.3-cli-alpine-supervisor
- suyar/php:7.3-cli-cron
- suyar/php:7.3-cli-alpine-cron
- suyar/php:7.4-cli-supervisor
- suyar/php:7.4-cli-alpine-supervisor
- suyar/php:7.4-cli-cron
- suyar/php:7.4-cli-alpine-cron
- suyar/php:8.0-cli-supervisor
- suyar/php:8.0-cli-alpine-supervisor
- suyar/php:8.0-cli-cron
- suyar/php:8.0-cli-alpine-cron
- suyar/php:8.1-cli-supervisor
- suyar/php:8.1-cli-alpine-supervisor
- suyar/php:8.1-cli-cron
- suyar/php:8.1-cli-alpine-cron

## 集成镜像

这些镜像都是从『主要镜像』构建的，包含 `php-fpm`、`supervisor` 和 `cron`，其中 `php-fpm` 和 `cron` 使用 `supervisor` 管理。

- suyar/php:7.0-integration
- suyar/php:7.0-alpine-integration
- suyar/php:7.1-integration
- suyar/php:7.1-alpine-integration
- suyar/php:7.2-integration
- suyar/php:7.2-alpine-integration
- suyar/php:7.3-integration
- suyar/php:7.3-alpine-integration
- suyar/php:7.4-integration
- suyar/php:7.4-alpine-integration
- suyar/php:8.0-integration
- suyar/php:8.0-alpine-integration
- suyar/php:8.1-integration
- suyar/php:8.1-alpine-integration

## 使用镜像

```
docker pull suyar/php:8.1-fpm
```

镜像仓库 [https://hub.docker.com/r/suyar/php](https://hub.docker.com/r/suyar/php)

> 更多用法请参考 [官方镜像](https://hub.docker.com/_/php)

## 预装扩展

预装扩展请以对应镜像的 `Dockerfile` 文件为准。

```
docker run --rm suyar/php:8.1-cli php -m

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
