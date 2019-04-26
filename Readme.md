# Ministrare`s Laradock Starters Template

## Table of contents

- [Description](#Description)
- [How to install](#How-to-install)
- [Credits](#Credits)
- [Author](#Author)

## Description
This project consist off a ready to use:
- [Laradock](https://laradock.io/) - laravel server based on docker containers, consists off:
    - [nginx](https://hub.docker.com/_/nginx)
    - [mariadb](https://hub.docker.com/_/mariadb)
    - [phpmyadmin](https://hub.docker.com/r/phpmyadmin/phpmyadmin)
- [Laravel](https://github.com/laravel/laravel) - php framework project folder

## Dependencies
In order to use the full functionality of this package, you`ll need a couple of programs already installed on your machine:
- [Github]()
- [Docker]()


## How to install
1. git clone https://github.com/ministrare/laradock-starters-template.git
1. git submodule update --recursive --remote
1. Open terminal and execute the following commands:
    ```
    cp .env.example-laradock laradock/.env
    cp docker-compose-laradock-example.yml laradock/docker-compose.yml
    cp .env.example-laravel laravel/.env
    cd laradock
    docker-compose up -d nginx mariadb phpmyadmin
    docker exec -it laradock_project_workspace_1 bash
    composer install
    php artisan key:generate
    php artisan migrate
    ```
1. Open your browser and go to localhost.

## Credits
Special thanks to Laravel Team!

## Author
This repository is created and updated by **Ministrare: Lesley Forn**. \
**Last update: 25/04/2019**