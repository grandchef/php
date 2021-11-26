# GrandChef - Composer Image for Development
Imagem base para desenvolver a aplicação php.

## Build

Criar imagem base
```sh
docker build -t grandchef/php:7.4.26-fpm-dev fpm-dev
```

Roda o shell na imagem criada
```sh
docker run -it --rm grandchef/php:7.4.26-fpm-dev /bin/sh
```

## Release

Envia imagem para o hub.docker
```sh
docker push grandchef/php:7.4.26-fpm-dev
```
