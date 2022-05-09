FROM nginxinc/nginx-unprivileged:1.21-alpine

ARG TARGET_ENVIRONMENTS

RUN echo "TARGET_ENVIRONMENTS: ${TARGET_ENVIRONMENTS}"

WORKDIR /app

USER root

RUN apk update && apk add --upgrade curl libgcrypt

COPY ./web .

COPY nginx.conf /etc/nginx/conf.d/default.conf

USER 65534

EXPOSE 3000
