# php-7.3.8-fpm

## php -v

```
PHP 7.3.14 (cli) (built: Feb  2 2020 20:52:18) ( NTS )
Copyright (c) 1997-2018 The PHP Group
Zend Engine v3.3.14, Copyright (c) 1998-2018 Zend Technologies
```

## php --ini

```
n
```

## php -m

> 由于某些时候，`gmagick` 和 `imagick` 扩展会出现冲突，所以默认未安装 `imagick`，如果需要安装，请自行使用 `docker-php-install imagick` 命令进行安装

```
apc
apcu
bcmath
bz2
calendar
Core
ctype
curl
date
dom
event
exif
fileinfo
filter
ftp
gd
gettext
gmp
hash
hrtime
iconv
igbinary
intl
json
libxml
lzf
mbstring
mcrypt
memcached
msgpack
mysqli
mysqlnd
openssl
pcntl
pcre
PDO
pdo_mysql
pdo_sqlite
Phar
posix
readline
redis
Reflection
session
shmop
SimpleXML
sockets
SPL
sqlite3
standard
timezonedb
tokenizer
xml
xmlreader
xmlwriter
zip
zlib

[Zend Modules]
```
