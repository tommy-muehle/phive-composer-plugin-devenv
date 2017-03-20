# phive-composer-plugin-devenv

Development environment to create the Composer plugin for [PHIVE](https://phar.io/).  
Based on [Composer plugin devenv](https://github.com/tommy-muehle/php-composer-plugin-devenv).

## Install

```
git clone https://github.com/tommy-muehle/phive-composer-plugin-devenv
cd phive-composer-plugin-devenv
git submodule update --init --recursive
cd plugin
composer update
```

## Usage

```
docker-compose run --rm composer global require phar-io/composer-plugin
```
