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

### Install the plugin

```
docker-compose run --rm composer global require phar-io/composer-plugin --prefer-dist
```

### Update the plugin (for example to add further dependencies)

```
docker-compose run --rm composer update --prefer-dist
```

### Run tests

Requires an existing "phpunit" executable in the bin directory (plugin/bin).

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
