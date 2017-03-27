FROM php:5.6-alpine
MAINTAINER Tommy Muehle <tommy.muehle@gmail.com>

RUN apk update --no-cache \
    && apk add --no-cache gnupg \
    && rm -rf /var/cache/apk/* /var/tmp/* /tmp/*

VOLUME ["/app"]
WORKDIR /app

CMD ["php", "-a", "-d", "date.timezone='Europe/Berlin'"]