# GrandChef - PHP Base Image with Nginx
Imagem base com php-fpm e nginx.

## Build

Criar imagem
```sh
docker build -t grandchef/php:7.4.15-nginx deploy/nginx
```

Roda o shell na imagem criada
```sh
docker run -it --rm grandchef/php:7.4.15-nginx /bin/bash
```

## Release

Envia imagem para o hub.docker
```sh
docker push grandchef/php:7.4.15-nginx
```
