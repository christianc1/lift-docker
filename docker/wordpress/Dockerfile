FROM alpine:latest

RUN apk add --no-cache curl

# Setup fs structure

WORKDIR /var/www/public

ENV WORDPRESS_VERSION 4.6.1
ENV WORDPRESS_SHA1 027e065d30a64720624a7404a1820e6c6fff1202

# Download WordPress.
RUN curl -o wordpress.tar.gz -SL https://wordpress.org/wordpress-4.6.1.tar.gz \
    && echo "$WORDPRESS_SHA1 *wordpress.tar.gz" | sha1sum -c - \
    && tar -xzf wordpress.tar.gz -C /var/www/public/ \
    && rm wordpress.tar.gz

CMD tail -f /dev/null