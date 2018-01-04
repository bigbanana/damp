## 特性
* 兼容www项目的php yaf框架
* 兼容多版本php带来的切换问题
* 兼容本地https访问
* 兼容docker网络导致的inner.yaozh.com不一致问题

### 依赖
* docker(请添加国内镜像，如阿里云镜像加速)
* docker-compose

### 服用须知
* 项目目录在damp目录同级
* vhost配置在apache2/sites
* php.ini在php-fpm目录，修改时请对应版本
* 默认环境为php7.1，若需要使用php5.6参考www.yaozh.com.conf apache配置
* mysql 数据目录在~/.damp/data

### 快速服用
``` bash
git clone git@lab.yaozh.com:yaozh/damp.git
cd damp
# set env
cp env-example .env
# build
docker-compose up -d
# rebuild
docker-compose build
# start
docker-compose start
# stop
docker-compose stop
# restart
docker-compose restart
# remove
docker-compose down
