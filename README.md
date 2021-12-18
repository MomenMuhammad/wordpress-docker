# Basic Docker Environment For Laravel
Basic Docker Configuration for laravel project

# Docker Images Included
- wordpress:5.8.2-php8.0-apache
- mariadb:10.4.22

# Steps
1. Go to your project
2. clone this repo as a submodule by doing ```git submodule add git@github.com:MomenMuhammad/wordpress-docker.git docker```
3. Go to the submodule folder ```cd docker```
4. create new .env file by copying the .env.example ```cp .env.exmpale .env``` for more information about [ENV variables](#env-variables-description)
5. edit the .env as you like
6. run ```docker-compose up -d```

# ENV variables description
## MARIADB Variables
- ```MARIADB_PORT ``` : Mariadb port number (outside the container)
- ```MARIADB_RANDOM_ROOT_PASSWORD ``` : Set root user password randomly (1 or 0)
- ```MARIADB_DATABASE_FILES_PATH``` : database's files path
## WordPress
- ```WORDPRESS_DB_HOST``` : Database host name which is mariadb by default
- ```WORDPRESS_DB_USER``` : Database username
- ```WORDPRESS_DB_PASSWORD``` : Database password
- ```WORDPRESS_DB_NAME``` : Database name
- ```WORDPRESS_TABLE_PREFIX``` : Wordpress table prefix 
- ```WORDPRESS_HTTP_PORT ``` : External apache port number HTTP (outside the container)
- ```WORDPRESS_HTTPS_PORT ``` : External apache port number HTTPS (outside the container)