FROM alpine:3.7

LABEL description="squid server"
LABEL maintainer="github@compuix.com"

RUN set -xe \
    && apk add --no-cache squid \
    && mkdir -p /var/cache/squid \
    && chown -R squid:squid /var/cache/squid

COPY squid.conf /etc/squid/squid.conf
COPY entrypoint.sh /usr/bin/entrypoint.sh

USER squid

ENTRYPOINT ["squid", "-NYC"]
