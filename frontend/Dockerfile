FROM nginxinc/nginx-unprivileged:1.20-alpine

WORKDIR /app

USER root

RUN apk update && apk add --upgrade curl libgcrypt

COPY ./web .

COPY nginx.conf /etc/nginx/conf.d/default.conf

USER 65534

EXPOSE 3000
