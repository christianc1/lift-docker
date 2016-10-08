FROM alpine:latest

RUN apk add --no-cache git

WORKDIR /var/www/public

ENV WORDPRESS_VERSION 4.6.1
ENV WORDPRESS_SHA1 027e065d30a64720624a7404a1820e6c6fff1202

# Download WordPress.
RUN git clone --depth=1 https://github.com/wordpress/wordpress.git wordpress

CMD tail -f /dev/null