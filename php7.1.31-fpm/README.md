# php-7.1.31-fpm

## php -v

```
PHP 7.1.31 (cli) (built: Aug  8 2019 15:21:01) ( NTS )
Copyright (c) 1997-2018 The PHP Group
Zend Engine v3.1.0, Copyright (c) 1998-2018 Zend Technologies
    with Zend OPcache v7.1.31, Copyright (c) 1999-2018, by Zend Technologies
```

## php --ini

```
Configuration File (php.ini) Path: /usr/local/etc/php
Loaded Configuration File:         /usr/local/etc/php/php.ini
Scan for additional .ini files in: /usr/local/etc/php/conf.d
Additional .ini files parsed:      /usr/local/etc/php/conf.d/amqp.ini,
/usr/local/etc/php/conf.d/apcu.ini,
/usr/local/etc/php/conf.d/cmark.ini,
/usr/local/etc/php/conf.d/ds.ini,
/usr/local/etc/php/conf.d/event.ini,
/usr/local/etc/php/conf.d/gmagick.ini,
/usr/local/etc/php/conf.d/grpc.ini,
/usr/local/etc/php/conf.d/hrtime.ini,
/usr/local/etc/php/conf.d/igbinary.ini,
/usr/local/etc/php/conf.d/libsodium.ini,
/usr/local/etc/php/conf.d/lzf.ini,
/usr/local/etc/php/conf.d/memcache.ini,
/usr/local/etc/php/conf.d/memcached.ini,
/usr/local/etc/php/conf.d/mongodb.ini,
/usr/local/etc/php/conf.d/msgpack.ini,
/usr/local/etc/php/conf.d/oauth.ini,
/usr/local/etc/php/conf.d/opcache.ini,
/usr/local/etc/php/conf.d/rar.ini,
/usr/local/etc/php/conf.d/redis.ini,
/usr/local/etc/php/conf.d/solr.ini,
/usr/local/etc/php/conf.d/ssh2.ini,
/usr/local/etc/php/conf.d/stomp.ini,
/usr/local/etc/php/conf.d/svm.ini,
/usr/local/etc/php/conf.d/swoole.ini,
/usr/local/etc/php/conf.d/sync.ini,
/usr/local/etc/php/conf.d/timezonedb.ini,
/usr/local/etc/php/conf.d/varnish.ini,
/usr/local/etc/php/conf.d/xlswriter.ini,
/usr/local/etc/php/conf.d/yaf.ini,
/usr/local/etc/php/conf.d/yaml.ini,
/usr/local/etc/php/conf.d/yar.ini,
/usr/local/etc/php/conf.d/zookeeper.ini
```

## php -m

> 由于某些时候，`gmagick` 和 `imagick` 扩展会出现冲突，所以默认未安装 `imagick`，如果需要安装，请自行使用 `docker-php-install imagick` 命令进行安装

```
[PHP Modules]
amqp
apc
apcu
bcmath
bz2
calendar
cmark
Core
ctype
curl
date
dba
dom
ds
event
exif
fileinfo
filter
ftp
gd
gettext
gmagick
gmp
grpc
hash
hrtime
iconv
igbinary
imap
intl
json
ldap
libxml
lzf
mbstring
mcrypt
memcache
memcached
mongodb
msgpack
mysqli
mysqlnd
OAuth
odbc
openssl
pcntl
pcre
PDO
pdo_mysql
PDO_ODBC
pdo_sqlite
Phar
posix
rar
readline
redis
Reflection
session
shmop
SimpleXML
soap
sockets
sodium
solr
SPL
sqlite3
ssh2
standard
Stomp
svm
swoole
sync
sysvmsg
sysvsem
sysvshm
timezonedb
tokenizer
varnish
xlswriter
xml
xmlreader
xmlrpc
xmlwriter
xsl
yaf
yaml
yar
Zend OPcache
zip
zlib
zookeeper

[Zend Modules]
Zend OPcache
```
