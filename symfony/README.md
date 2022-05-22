## Introduction

Build a simple laravel development environment with docker-compose. Compatible with Windows(WSL2), macOS(M1) and Linux.

## Usage

```bash
$ make create-project # Install the Symfony project
```

http://localhost:8080

## Tips

- Read this Makefile

## Container structures

```bash
├── app
├── web
└── db
```

### app container

- Base image
  - [php](https://hub.docker.com/_/php):8.0-fpm
  - [composer](https://hub.docker.com/_/composer):2.2

### web container

- Base image
  - [nginx](https://hub.docker.com/_/nginx):1.20

### db container

- Base image
  - [mysql/mysql-server](https://hub.docker.com/r/mysql/mysql-server):8.0