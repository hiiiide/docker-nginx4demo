FROM alpine:3.16

# install nginx
RUN apk update && \
    apk add --no-cache nginx

# set root dir
ADD app /app
ADD default.conf /etc/nginx/conf.d/default.conf

# set port
EXPOSE 80
RUN mkdir -p /run/nginx

# run nginx
CMD nginx -g "daemon off;"
