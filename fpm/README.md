# GrandChef - PHP FPM Image
Imagem base para criação de container.

## Build

Criar imagem base
```sh
docker build -t grandchef/php:8.2.2-fpm-alpine fpm
```

Roda o shell na imagem criada
```sh
docker run -it --rm grandchef/php:8.2.2-fpm-alpine /bin/sh
```

## Release

Envia imagem para o hub.docker
```sh
docker push grandchef/php:8.2.2-fpm-alpine
```
