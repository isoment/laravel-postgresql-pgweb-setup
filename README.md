## Docker Setup for Laravel with PostgreSQL

A docker setup utilizing PHP, Nginx, PostgreSQL and Pgweb that can be used with Laravel. There is a sample .env
file you can modify to suit your needs. 

## Usage

Download [Laravel](https://github.com/laravel/laravel) and copy the docker files into your application folder, run

```
docker-compose up
```

Run the following to find the container id of the php container

```
docker ps
```

Start a shell on the php container

```
docker exec -it <container id> /bin/sh
```

Install composer dependencies

```
composer install
```

Generate a new application key

```
php artisan key:generate
```

Install and compile JS dependencies

```
yarn
yarn dev
```

You can access the project at

```
localhost:8008
```

Login to pgweb, no password by default...

```
localhost:8081

Host: postgres
Username: root
Database: laravel
SSL Mode: disable
```

If the are on linux you may have to change the permissions of the Laravel storage directory or modify the
docker files accordingly.