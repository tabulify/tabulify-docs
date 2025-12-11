# Tabulify.com


## About

This Git repo contains [tabulify.com](https://www.tabulify.com) written with the [Combo Site Technology](https://www.combostrap.com/admin/combostrap-website-yfi22ewn)


## How to run locally with docker


```bash
docker run \
  --name site-com-tabulify \
  --rm \
  -p 8081:80 \
  --user 1000:1000 \
  -e DOKU_DOCKER_ENV=dev \
  -e DOKU_DOCKER_ACL_POLICY='public' \
  -e DOKU_DOCKER_ADMIN_NAME='admin' \
  -e DOKU_DOCKER_ADMIN_PASSWORD='welcome' \
  -e DOKU_DOCKER_GIT_SITE='https://github.com/tabulify/tabulify-docs' \
  -v $PWD:/var/www/html \
  ghcr.io/combostrap/dokuwiki:php8.3-latest
```

