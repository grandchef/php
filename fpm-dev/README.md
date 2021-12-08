# GrandChef - Composer Image for Development
Imagem base para desenvolver a aplicação php.

## Build

Criar imagem base
```sh
docker build -t grandchef/php:8.1.0-fpm-dev fpm-dev
```

Roda o shell na imagem criada
```sh
docker run -it --rm grandchef/php:8.1.0-fpm-dev /bin/sh
```

## Release

Envia imagem para o hub.docker
```sh
docker push grandchef/php:8.1.0-fpm-dev
```
