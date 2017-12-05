FROM nginx:1.13-alpine

RUN set -ex \
    && addgroup -g 1000 yii2 \
    && adduser -u 1000 -D -H -G yii2 -s /bin/sh yii2 \
    && apk update \
    && apk --no-cache add --update openssl

COPY etc/nginx /etc/nginx

WORKDIR /var/www

CMD ["nginx", "-g", "daemon off;"]

EXPOSE 80 443