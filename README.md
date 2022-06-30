# docker-base-laravel9
Estrutura base para PHP 8.1.1 - Laravel 9 - Mysql - Redis

#gerar o .env e editar
APP_NAME=EspecializaTi
APP_URL=http://localhost:8989

DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=nome_que_desejar_db
DB_USERNAME=root
DB_PASSWORD=root

CACHE_DRIVER=redis
QUEUE_CONNECTION=redis
SESSION_DRIVER=redis

REDIS_HOST=redis
REDIS_PASSWORD=null
REDIS_PORT=6379

#subir os containers
docker-compose up -d

#acessar o container app
docker-compose exec app bash

#instalar as dependencias
composer install

#gerar a key do laravel
php artisan key:generate

#acessar
http://localhost:8989

Fonte https://github.com/especializati/setup-docker-laravel/tree/laravel-9-com-php-8
