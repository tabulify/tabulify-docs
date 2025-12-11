# Contribution

## Steps

### Clone

> [!IMPORTANT]
> If you are not member of the Tabulify Organisation, you need to create and clone a fork.

* Only this repository
```bash
# without the tabulify code
git clone git@github.com:tabulify/tabulify-docs.git
cd tabulify-docs
```
* With the tabulify repository (as it is a [submodules](https://github.com/tabulify/tabulify/.gitmodules))
```bash
git clone --recurse-submodules https://github.com/tabulify/tabulify
cd docs-tabul
```


### Run

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

* With SSH key, change use the following URI
```bash
-e DOKU_DOCKER_GIT_SITE='git@github.com:tabulify/tabulify-docs.git'
```
