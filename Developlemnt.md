# setup mysql
```
docker run --rm -p 3306:3306 -it -e MYSQL_ROOT_PASSWORD=root mysql:5.7 bash
service mysql start
create database shop;
create user opencart;
grant all on shop.* to 'opencart'@'%' identified by 'opencart';
flush privileges;
exit
```
# Install
```
php cli_install.php install --http_server http://localhost/ --db_hostname mysql --db_username opencart --db_password opencart --username admin --password admin --email phammanh029@gmail.com --db_database shop
```