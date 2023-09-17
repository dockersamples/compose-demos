# compose-demos


## Table of Content

- [Docker Compose: A Simple WordPress App Demo](https://github.com/ajeetraina/compose-demos/blob/main/wordpress/README.md)
- [Compose and Secrets: Wordpress App](https://github.com/ajeetraina/compose-demos/tree/main/wordpress/secrets/README.md)

## A Simple Run command for DB

```
docker run -d --name db \
  -e MYSQL_ROOT_PASSWORD=somewordpress \
  -e MYSQL_DATABASE=wordpress \
  -e MYSQL_USER=wordpress \
  -e MYSQL_PASSWORD=wordpress \
  -v db_data:/var/lib/mysql \
  -p 3306:3306 \
  mariadb:10.6.4-focal
```


## A Simple Run command for Wordpress


```
docker run -d --name wordpress \
  -e WORDPRESS_DB_HOST=db \
  -e WORDPRESS_DB_USER=wordpress \
  -e WORDPRESS_DB_PASSWORD=wordpress \
  -e WORDPRESS_DB_NAME=wordpress \
  -p 80:80 \
  wordpress:latest
```

