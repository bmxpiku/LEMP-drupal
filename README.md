##drupal7 on PHP 7.2 + MySQL 8.0.12 + Nginx + Memcached 


Hello this is stack on four separate containers ..

### TODO


###TO RUN this
prior running docker please update path in 
\phpdocker\nginx\yousite_name.conf

just type in console 
docker-compose up -d

#### for fresh drupal8 installation
1. docker exec -it drupal-php-fpm bash
2. cd /var/www
3. mkdir drupal8
4. composer create-project drupal-composer/drupal-project:8.x-dev drupal8 --stability dev --no-interaction
 - more info about installing via composer here https://www.drupal.org/docs/develop/using-composer/using-composer-to-manage-drupal-site-dependencies#download-core
5. By default database named d8 is created but you can make new one by (in mysql container)
 - mysql -uroot -proot -e "CREATE DATABASE databasename CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci";
 - [IMPORTANT] mysql --user=root --password=root --execute="ALTER USER 'root'@'%' IDENTIFIED WITH mysql_native_password BY 'root';"
6. use root user for local dev or create one with:
 - CREATE USER username@localhost IDENTIFIED BY 'password';
 - GRANT ALL PRIVILEGES ON databasename.* TO 'username'@'localhost';
7. Visit your site in a web browser. You should be redirected to the installer page at `/core/install.php`
8. status check https://www.drupal.org/docs/8/install/step-6-status-check
#### for existing db:
Add mysql db with 
pv Dump20181022.sql | mysql -uroot -proot -hmysql

And youre good to go.

Profit!
