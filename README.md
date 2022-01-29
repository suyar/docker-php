# Docker Images For PHP

## 仓库概述

基于官方镜像的 php 镜像，已安装常用扩展

> 官方 PHP 版本生命周期参考 [PHP 版本支持](https://www.php.net/supported-versions.php)

- [`PHP` 官方镜像](https://hub.docker.com/_/php)
- [扩展安装工具](https://github.com/mlocati/docker-php-extension-installer)
- 基于 `GitHub Actions` 每周自动构建 `0 12 * * 6`

## 构建镜像

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

## 使用镜像

```
docker pull suyar/php:8.1-fpm
```

镜像仓库 [https://hub.docker.com/r/suyar/php](https://hub.docker.com/r/suyar/php)

> 更多用法请参考 [官方镜像](https://hub.docker.com/_/php)

## 预装扩展

预装扩展请以对应镜像的 Dockerfile 文件为准

```
docker exec --rm suyar/php:8.0-cli php -m

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
