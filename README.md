# Docker Images For PHP

## 概述

基于官方镜像的 php 镜像


- [基础镜像](https://hub.docker.com/_/php)
- [扩展安装](https://github.com/mlocati/docker-php-extension-installer)

## 镜像

- suyar/php:7.0-fpm
- suyar/php:7.0-cli
- suyar/php:7.1-fpm
- suyar/php:7.1-cli
- suyar/php:7.2-fpm
- suyar/php:7.2-cli
- suyar/php:7.3-fpm
- suyar/php:7.3-cli
- suyar/php:7.4-fpm
- suyar/php:7.4-cli
- suyar/php:8.0-fpm
- suyar/php:8.0-cli
- suyar/php:8.1-fpm
- suyar/php:8.1-cli

## 获取

```
docker pull suyar/php:8.1-fpm
```

镜像仓库 [https://hub.docker.com/r/suyar/php](https://hub.docker.com/r/suyar/php)

## 用法

[同官方镜像](https://hub.docker.com/_/php)

## 扩展

```
docker exec --rm suyar/php:8.1-cli php -m
```
