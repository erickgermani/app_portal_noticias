# Instruções para executar o projeto

Este projeto é uma aplicação web em Laravel que exibe as dez primeiras notícias armazenadas em um banco de dados populados com mil exemplos. Por fins de performance, o Redis está configurado para persistir os dez primeiros dados em cachê por quinze segundo. Para executar o projeto, siga as instruções abaixo:

## Pré-requisitos

* PHP 7.3 ou superior
* MySQL 5.7 ou superior
* Composer
* Redis

## Configuração do banco de dados

1. Crie um banco de dados vazio no seu servidor MySQL.
2. Renomeie o arquivo .env.example para .env.
3. Abra o arquivo .env e altere as informações de conexão com o banco de dados de acordo com as configurações do seu servidor MySQL

```makefile
APP_NAME="Portal de Noticias"
APP_ENV=local
APP_KEY=
APP_DEBUG=true
APP_URL=http://localhost

LOG_CHANNEL=stack
LOG_DEPRECATIONS_CHANNEL=null
LOG_LEVEL=debug

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=
DB_USERNAME=
DB_PASSWORD=

BROADCAST_DRIVER=log
CACHE_DRIVER=redis
FILESYSTEM_DISK=local
QUEUE_CONNECTION=sync
SESSION_DRIVER=file
SESSION_LIFETIME=120

MEMCACHED_HOST=127.0.0.1

REDIS_HOST=127.0.0.1
REDIS_PASSWORD=null
REDIS_PORT=6379
REDIS_CLIENT=predis

PUSHER_PORT=443
PUSHER_SCHEME=https
PUSHER_APP_CLUSTER=mt1

VITE_PUSHER_APP_KEY="${PUSHER_APP_KEY}"
VITE_PUSHER_HOST="${PUSHER_HOST}"
VITE_PUSHER_PORT="${PUSHER_PORT}"
VITE_PUSHER_SCHEME="${PUSHER_SCHEME}"
VITE_PUSHER_APP_CLUSTER="${PUSHER_APP_CLUSTER}"
```

## Instalação das dependências

1. Abra o terminal e navegue até a pasta raiz do projeto.
2.  Execute o comando composer install para instalar as dependências do projeto.

## Criação e população do banco de dados

1. Ainda no terminal e na pasta raiz do projeto, execute o comando php artisan migrate para criar as tabelas do banco de dados.
2. Em seguida, execute o comando php artisan db:seed para popular o banco de dados com notícias fictícias.

## Execução do Redis

1. Certifique-se de que o Redis está instalado e em execução no seu sistema operacional.
2. Abra um novo terminal e execute o comando redis-server para iniciar o servidor Redis.

## Execução do Laravel

1. No terminal e na pasta raiz do projeto, execute o comando php artisan serve para iniciar o servidor web do Laravel.
2. Abra um navegador e acesse a URL http://localhost:8000. Você deverá ver as dez primeiras notícias exibidas na página.

## Conclusão

Seguindo essas instruções, você deverá conseguir executar o projeto em seu ambiente local. Qualquer dúvida ou problema, por favor, consulte a documentação oficial do Laravel em https://laravel.com/docs.
