FROM mysql 
MAINTAINER wanyux

# Initial the DB 
COPY mysql.sql ./
CMD mysql -hmysql-server -uroot -ppassword < mysql.sql 
