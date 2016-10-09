FROM alpine:latest

RUN apk add --no-cache git

WORKDIR /var/www/public/wp-content/mu-plugins

RUN git clone --recursive https://github.com/automattic/vip-mu-plugins-public.git .

CMD tail -f /dev/null