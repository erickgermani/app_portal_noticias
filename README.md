# Instruções para executar o projeto

Este projeto é uma aplicação web em Laravel que exibe as dez primeiras notícias armazenadas em um banco de dados populados com mil exemplos. Por fins de performance, o Redis está configurado para persistir os dez primeiros dados em cachê por quinze segundo. Para executar o projeto, siga as instruções abaixo:

## Pré-requisitos

* PHP 7.3 ou superior
* MySQL 5.7 ou superior
* Composer
* Redis

## Configuração do banco de dados

1. Crie um banco de dados vazio no seu servidor MySQL.
2. Renomeie o arquivo `.env.example` para `.env`.
3. Abra o arquivo `.env` e altere as informações de conexão com o banco de dados de acordo com as configurações do seu servidor MySQL

## Instalação das dependências

1. Abra o terminal e navegue até a pasta raiz do projeto.
2. Execute o comando `composer install` para instalar as dependências do projeto.

## Criação e população do banco de dados

1. Ainda no terminal e na pasta raiz do projeto, execute o comando `php artisan migrate` para criar as tabelas do banco de dados.
2. Em seguida, execute o comando `php artisan db:seed` para popular o banco de dados com notícias fictícias.

## Execução do Redis

1. Certifique-se de que o Redis está instalado e em execução no seu sistema operacional.
2. Abra um novo terminal e execute o comando `redis-server` para iniciar o servidor Redis.

## Execução do Laravel

1. No terminal e na pasta raiz do projeto, execute o comando php artisan serve para iniciar o servidor web do Laravel.
2. Abra um navegador e acesse a URL `http://localhost:8000`. Você deverá ver as dez primeiras notícias exibidas na página.

## Conclusão

Seguindo essas instruções, você deverá conseguir executar o projeto em seu ambiente local. Qualquer dúvida ou problema, por favor, consulte a documentação oficial do Laravel em https://laravel.com/docs.
