# devops-june2018
## Docker Installation
https://docs.docker.com/install/
## Hello World
`docker run hello-world`
## Wordpress
### Mysql
`docker run -d --name devops-mysql -e MYSQL_ROOT_PASSWORD=FunnyMonkeyCow mysql:5.7 `
### Wordpress
`docker run -d --name devops-wordpress -p 8080:80 --link devops-mysql:mysql -e WORDPRESS_DB_PASSWORD=FunnyMonkeyCow wordpress`
### Stop and remove
`docker rm -f devops-mysql devops-wordpress`
## Docker Compose
`docker-compose up -d`

`docker-compose rm --stop`