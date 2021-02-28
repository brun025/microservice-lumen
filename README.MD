# Docker infrastructure for Lumen 

![](https://img.shields.io/badge/version-1.0.0-green.svg)
![](https://img.shields.io/badge/docker--compose-build-blue.svg)
![](https://img.shields.io/badge/docker-build-blue.svg)

### Description

Microservice Lumen is a starting skeleton based on Docker and Lumen Framework. This project helps to develop and maintain a simple and clean infrastructure for the management / creation of php microservices. In just a few steps, the developer starts the development / production environment as needed.
Basically, the Nginx containers are available for the webserver, the backend container in PHP 7.4 for the application, both based on Linux alpine. Include MySQL container by default.
The Dockefile (in the docker folder) is already set up to create the production image of the application, we recommend modifying it only to add dependencies or configurations.

**- require**
    
    OS: linux
    Packages: make
    Docker version: >= 18.09.6
    docker-compose version: >= 1.28.0

**- setup and run**

    1.  make setup

    2.  Set .env db connection into source:
        DB_CONNECTION=mysql
        DB_HOST=database
        DB_PORT=3306
        DB_DATABASE=lumen
        DB_USERNAME=root
        DB_PASSWORD=root
    
**- make commands**

    down:  down containers

    up:   up -d containers

    exec:  enter in app container

    exec_mysql:  enter in database container

    ssh_root:  connection ssh (as root) to server

    ssh:  connection ssh (as www-data) to server

    deploy: rebuild containers (down, build and up)

    ## production ##

    image_build:  build immagine

    image_push: publish image


[Manual push](https://docs.docker.com/engine/reference/commandline/push/) into docker hub registry

### References 
    
**Nginx**: 1.18

**PHP**: 7.4-fpm-alpine

**MySQL**: 8.0

## License

This project is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT)
