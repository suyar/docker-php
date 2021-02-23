# Docker Image For PHP

## 概述

- 镜像仅用于开发测试环境使用，附带了大部分常用扩展，如果需要其他扩展，请提交相关 `Issue` 或 `PR`
- 请勿使用本镜像直接作为生产的镜像使用，因为 `php-fpm` 默认使用 `root` 用户运行
- 如果不需要太多扩展，请自己重新构建，在 `Dokcerfile` 删掉不需要安装的扩展就行
- 预装的扩展一律使用 `commit` 时能装的最新版本，如果需要其他版本，请自己重新构建
- 镜像基于 `centos:8`，并且没有保留 PHP 源码
- 不对镜像的大小做限制，故而镜像里包含很多常用的命令

## 镜像列表

> 不再支持 `PHP7.4` 以下版本的构建

- [`php74`](php74/README.md)
- [`php80`](php80/README.md)

## 获取镜像

```
docker pull suyar/php:74
docker pull suyar/php:80
```

镜像仓库 [https://hub.docker.com/r/suyar/php](https://hub.docker.com/r/suyar/php)

## 环境变量

```
PHP_VERSION=x.x.x
PHP_PREFIX=/usr/local/php
PHP_BIN_DIR=/usr/local/bin
PHP_SBIN_DIR=/usr/local/sbin
PHP_INI_DIR=/usr/local/php/etc
PHP_INI_SCAN_DIR=/usr/local/php/etc/conf.d
PHP_FPM_DIR=/usr/local/php/etc
PHP_FPM_SCAN_DIR=/usr/local/php/etc/php-fpm.d
PHP_EXT_DIR=/usr/local/php/ext
```

## 用法

- 如果直接用作 `php-fpm`，直接 `docker run -d suyar/php:xx`
- 如果用作 `cli` 的，直接 `docker run -it --rm suyar/php:xx php -v`

## 预装扩展

- 详细的内容请看对应 PHP 版本的 README 文件
- 如果需要安装其他扩展，可以参考 `docker-php-install` 文件
