FROM alpine:latest

RUN set -ex \
    && addgroup -g 1000 yii2 \
    && adduser -u 1000 -D -H -G yii2 -s /bin/sh yii2

USER yii2

WORKDIR /var/www