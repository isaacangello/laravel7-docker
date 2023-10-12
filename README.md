
##### Introduction
This is a small project to run laravel 7 and mariadb, in docker using docker-compose.yml file, this aims to serve as a platform to study laravel based on the course

##### Requeriments and content
This project use:
 - [webdevops/php-nginx:7.4-alpine Docker image.](https://dockerfile.readthedocs.io/en/latest/content/DockerImages/dockerfiles/php-nginx.html)
 - [mariadb:11.1.2 Docker image.](https://hub.docker.com/_/mariadb)
 - [curso-completo-do-desenvolvedor-laravel files.](https://www.udemy.com/course/curso-completo-do-desenvolvedor-laravel/)

 This repository already contains a version of laravel 7 with a little project named by the super management author, so I need to run the composer update in the container, there is also a mysql dump file to create the database

##### Configuring and running the project

To run the project, some prior configurations are required:
You need to configure environment variables.
Mariadb docker image.
The mariadb environment variables are used in docker-compose.yml, and are referenced in the [maridadb](https://hub.docker.com/_/mariadb) official docker image documentation,
look for the "Environment Variables" section in the docker image documentation, these variables must be filled in the .env file in the same folder as the docker-compose.yml file,
Otherwise the image will not be compiled resulting in an infinite remainder.

    MARIADB_DATABASE={nomedobanco}
    MARIADB_ROOT_PASSWORD={passwdroot*}
    MARIADB_USER={user}
    MARIADB_PASSWORD={passwdroot*}

laravel environment variables
Laravel environment variables are referenced in the [laravel 7](https://laravel.com/docs/7.x/configuration#environment-configuration) documentation, despite
If the variables do not prevent the compilation of the docker image, it is advisable that you configure the values to access the database.

    DB_CONNECTION=mysql
    DB_HOST=dbhost
    DB_PORT=3306
    DB_DATABASE=sg
    DB_USERNAME=user
    DB_PASSWORD=passwdroot*


##### Introdução
Esse é um pequeno projeto para rodar o laravel 7 e mariadb, em docker usando arquivo  docker-compose.yml,  esse tem por objetivo servir de plataforma Para estudar o laravel com baso no curso
[curso completo do desenvolvedor laravel da udemy](https://www.udemy.com/course/curso-completo-do-desenvolvedor-laravel/) feito pelo [jorge San Aana](https://www.udemy.com/course/curso-completo-do-desenvolvedor-laravel/#instructor-1).

##### Requisitos e conteudo
Esse projeto usa:
 - [webdevops/php-nginx:7.4-alpine Docker image.](https://dockerfile.readthedocs.io/en/latest/content/DockerImages/dockerfiles/php-nginx.html)
 - [mariadb:11.1.2 Docker image.](https://hub.docker.com/_/mariadb)
 - [curso-completo-do-desenvolvedor-laravel arquivos.](https://www.udemy.com/course/curso-completo-do-desenvolvedor-laravel/)

Esse repositorio já contém  uma versão do laravel 7 com um projetinho nomeado pelo autor de super gestão então e preciso rodar no container o composer update, também já vem uma arquivo de dump mysql para criar o banco

##### Configurando e rodando projeto

Para rodar o projeto é necessário algumas configurações prévias:

É preciso configurar variáveis de ambiente.


Imagem docker do Mariadb.

As variáveis de ambiente do mariadb são usadas no docker-compose.yml, e são referenciadas na documentação da imagem docker oficial do [maridadb](https://hub.docker.com/_/mariadb) , 
procure a sessão "Environment Variables" na documentação da imagem docker, essas variáveis devem ser preenchidas no arquivo .env na mesma pasta do arquivo docker-compose.yml,
caso contrátio a imagem não será compilada resultando e em um restart infinito.

    MARIADB_DATABASE={nomedobanco}
    MARIADB_ROOT_PASSWORD={passwdroot*}
    MARIADB_USER={user}
    MARIADB_PASSWORD={passwdroot*}

Variáveis de ambiente do laravel:

As variáveis de ambiente do laravel são referenciadas na documenação do [laravel 7](https://laravel.com/docs/7.x/configuration#environment-configuration), a pesar   
das variáveis não impedirem a compilação da imagem docker, mas é aconselhável que você configure os valores para acessar o banco de dados.

    DB_CONNECTION=mysql
    DB_HOST=dbhost
    DB_PORT=3306
    DB_DATABASE=sg
    DB_USERNAME=user
    DB_PASSWORD=passwdroot*

