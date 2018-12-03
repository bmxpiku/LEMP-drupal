## After container is awake
mysql --user=root --password=root --execute="ALTER USER 'root'@'%' IDENTIFIED WITH mysql_native_password BY 'root';"
