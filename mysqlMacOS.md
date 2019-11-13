# MySQL

## Start service
/usr/local/bin/mysql.server restart

## How to Activate general log mysql

- sudo vim /etc/mysql/mysql.conf.d/mysqld.cnf
- uncomment these two lines :
```
general_log_file = /var/log/mysql/mysql.log
general_log = 1
```
- sudo service mysql restart

## Better displaying a query in terminal
```
SELECT * FROM user WHERE id = 1\G
```
