# phive-composer-plugin-devenv

Development environment to create the Composer plugin for [PHIVE](https://phar.io/).  
Based on [Composer plugin devenv](https://github.com/tommy-muehle/php-composer-plugin-devenv).

## Install

```
git clone https://github.com/tommy-muehle/phive-composer-plugin-devenv
cd phive-composer-plugin-devenv
git submodule update --init --recursive
```

## Usage

### Update the plugin to initialize

```
docker-compose run --rm composer global update --prefer-dist
```

### Run tests

Requires an existing "phpunit" executable in the bin directory ([plugin/bin](https://github.com/phar-io/composer-plugin/tree/c1a9b4fd6dedd67b44744616bfbcb3073f7670dd/bin)).

```
docker-compose run --rm plugin bin/phpunit -c phpunit.xml.dist
```

### Run PHPStan

```
docker-compose run --rm phpstan analyse src tests --level=5
```

### Run Humbug

```
docker-compose run --rm humbug
```
