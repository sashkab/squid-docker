FROM alpine:3.7

LABEL description="squid server"
LABEL maintainer="github@compuix.com"

RUN set -xe \
    && apk add --no-cache squid

# TODO ADD CONFIG
EXPOSE 3128
