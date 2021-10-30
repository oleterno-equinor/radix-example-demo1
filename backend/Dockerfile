FROM nginxinc/nginx-unprivileged:1.20.1-alpine

WORKDIR /app

COPY ./images ./images

COPY nginx.conf /etc/nginx/conf.d/default.conf

USER 65534

EXPOSE 6000
