# Mysql

## Basic Commands

### Mysql general
```
mysql> SHOW DATABASES;
mysql> DESCRIBE [DB-NAME];
mysql> USE [DB-NAME];
mysql> SHOW TABLES;
mysql> DESCRIBE [TABLE-NAME];
mysql> SELECT * FROM [TABLE-NAME];
mysql> SHOW COLUMNS FROM [TABLE-NAME];
mysql> SHOW VARIABLES LIKE `c%`;
mysql> SHOW STATUS;
```

### Accounts & passwords
```
$ mysql --version;
$ mysql -h localhost -P3306 -u [user-name] -p --protocol=tcp
```
```
mysql> USE MYSQL;	
mysql> SELECT HOST, USER, AUTHENTICATION_STRING FROM USER;
mysql> ALTER USER 'root'@'localhost' IDENTIFIED WITH MYSQL_NATIVE_PASSWORD BY 'new password';
```
