# Setup for Symfony Dockerized Project
Docker compose for symfony + mysql

## Docker containers:

		DataBase:
		 1. MySQL
		 2. PhpMyAdmin
		
		Server Code:
		 1. PHP
		 2. Apache


Usage
-----
Build
```bash
$ docker-compose build
$ docker-compose up -d
```
Show all container
```bash
$ docker-compose ps
```
Connect to container
```bash
$ docker exec -it www_tkt bash
```
Install composer and create database
```bash
$ cd tkt/
$ composer install
$ php bin/console doctrine:database:create
$ php bin/console doctrine:schema:update -f
$ exit
```

Run development environment
```bash
$ docker-compose up
```
or run in background
```bash
$ docker-compose up -d
```


Access to project
------------------

TKT: http://localhost:8742

Phpmyadmin: http://localhost:8082