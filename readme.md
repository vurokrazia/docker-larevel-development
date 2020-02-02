# Repositorio para ejecutar laravel con docker
Este repositorio lo creo con el fin de tener una base para ejecutar laravel, no tiene muchas configuraciones más que
* php
* composer
* mysql 
* nginx

## Configurar las variables de mysql con tú proyecto
Editar docker-compose.yml en mysql las siguientes variables con tus datos del proyecto
* ``` MYSQL_DATABASE: vurokrazia ```
* ``` MYSQL_USER: vurokrazia ```
* ``` MYSQL_PASSWORD: 123456 ```
* ``` MYSQL_ROOT_PASSWORD: 123456 ```
## Pasos para ejecutar la imagen con docker composer
* Abrir la terminal en el directorio del repositorio
* Descargar y compilar todo lo necesario ``` docker-compose build ```
* Levantar servicios ``` docker-compose up  ```
* Detener servicios ``` docker-compose down  ```

## Paso para restaurar base de datos con mysql
* Debes tener el archivo a restaurar con .sql
* cat backup.sql | docker exec -i CONTAINER /usr/bin/mysql -u root --password=root DATABASE

## Paso para crear respaldo base de datos con mysql
* Debes tener el archivo a restaurar con .sql
* docker exec CONTAINER /usr/bin/mysqldump -u root --password=root DATABASE > backup.sql

## Proyecto de larvel
Debes colocar tu proyecto en src, esta carpeta es la raiz asi que puedes iniciar el repositorio en src, hacer pull y configurar tu entorno.

[https://twitter.com/vurokrazia]("vurokrazia")
