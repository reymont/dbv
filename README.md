Database version control, made easy!
=

**dbv.php** is a database version control web application featuring schema management, revision scripts, and more!

Check out the **[project website](http://dbv.vizuina.com)** for more details, features and documentation.

[![dbv.php](http://dbv.vizuina.com/img/screenshot-main.png)](http://dbv.vizuina.com)


## 修改内容

取消了revisions中只列出数据的版本

## revisions



在[dbv]/data/revisions 目录下，新建子目录，子目录中包含.sql文件。

执行sql后，最后更新的版本会保存在 [dbv]/meta/revision 文件中

```sh
wget https://github.com/victorstanciu/dbv/archive/1.3.tar.gz
### 准备docker php
docker run -d -p 8180:80 --name php7 --privileged -v "$PWD":/var/www/html php:7.0-apache
docker exec -it php7 bash
### 安装pdo_mysql
docker-php-ext-install pdo_mysql mysqli
docker restart php7
### 修改权限
chown -R 33:33 ./
### config.conf
cp config.conf.sample
# define('DB_HOST', 'localhost');
# define('DB_PORT', 3306);
# define('DB_USERNAME', 'root');
# define('DB_PASSWORD', '123456');
# define('DB_NAME', '93zp');

```