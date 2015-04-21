jke-docker-sample
-----------------------------------  
Sample dockerized J2EE application
  
### Build 2 docker images for the web and db components
		cd db
		docker build -t jke/db .
		cd ../web
		docker build -t jke/web .

### Run the J2EE application with 3 docker containers
		docker run --name mysql-server -e MYSQL_ROOT_PASSWORD=password -d mysql
		docker run --link mysql-server:mysql-server -d jke/db
		docker run --link mysql-server:mysql-server -P -d jke/web

### Check the running JKE Banking running at http://192.168.27.100:8080
