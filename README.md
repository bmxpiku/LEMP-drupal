##drupal7 on PHP 7.2 + MySQL 8.0.12 + Nginx + Memcached 


Hello this is stack on four separate containers ..

### TODO
move this into dockerfiles

 - web
apt-get update
apt-get upgrade
apt-get install -y mysql-client nano curl
apt-get install -y pv

// let us setup prompt
export PS1="\[\e[32m\][\[\e[m\]\[\e[31m\]\u\[\e[m\]\[\e[33m\]@\[\e[m\]\[\e[32m\]\h\[\e[m\]:\[\e[36m\]\w\[\e[m\]\[\e[32m\]]\[\e[m\]\[\e[32;47m\]\\$\[\e[m\] "


 - mysql

apt-get update && apt-get upgrade && apt-get install -y procps

ALTER USER 'root'@'%' IDENTIFIED WITH mysql_native_password BY 'root';

###TO RUN this
prior running docker please update path in 
\phpdocker\nginx\yousite_name.conf

just type in console 
docker-compose up -d 

And youre good to go.

Profit!