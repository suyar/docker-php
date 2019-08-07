# Docker images for php

## 概述

- 镜像仅用于开发测试环境使用，附带了大部分常用扩展，如果需要其他扩展，请提交相关 Issue
- 请勿使用本镜像直接作为生产的镜像使用，因为 php-fpm 的用户和组默认为 root
- 如果不需要太多扩展，请自己重新构建，在 Dokcerfile 删掉不需要安装的扩展就行
- 预装的扩展一律使用当前能装的最新版本，如果需要其他版本，请自己重新构建
- 镜像基于 CentOS7，并且没有保留 PHP 源码
- 不对镜像的大小做限制，故而镜像里包含很多常用的命令

## 镜像列表

- [`php5.3.29-fpm`](php5.3.29-fpm/README.md) [`php5.3-fpm`](php5.3.29-fpm/README.md)
- [`php5.4.45-fpm`](php5.4.45-fpm/README.md) [`php5.4-fpm`](php5.4.45-fpm/README.md)
- [`php5.5.38-fpm`](php5.5.38-fpm/README.md) [`php5.5-fpm`](php5.5.38-fpm/README.md)
- [`php5.6.40-fpm`](php5.6.40-fpm/README.md) [`php5.6-fpm`](php5.6.40-fpm/README.md)
- [`php7.0.33-fpm`](php7.0.33-fpm/README.md) [`php7.0-fpm`](php7.0.33-fpm/README.md)
- [`php7.1.31-fpm`](php7.1.31-fpm/README.md) [`php7.1-fpm`](php7.1.31-fpm/README.md)
- [`php7.2.21-fpm`](php7.2.21-fpm/README.md) [`php7.2-fpm`](php7.2.21-fpm/README.md)
- [`php7.3.8-fpm`](php7.3.8-fpm/README.md) [`php7.3-fpm`](php7.3.8-fpm/README.md)

## 获取镜像

```
docker push carolkey/php:tagname
```

## 环境变量

```
PHP_VERSION=x.x.x
PHP_INI_DIR=/usr/local/etc/php
PHP_INI_SCAN_DIR=/usr/local/etc/php/conf.d
PHP_FPM_DIR=/usr/local/etc
PHP_FPM_SCAN_DIR=/usr/local/etc/php-fpm.d
```

## 预装扩展

详细的内容请看对应 PHP 版本的 README 文件
