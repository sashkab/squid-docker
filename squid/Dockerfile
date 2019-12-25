FROM alpine:3.11

LABEL \
    maintainer="github@compuix.com" \
    version="2019.12.25" \
    description="squid server."

RUN set -xe \
    && apk add --no-cache squid \
    && mkdir -p /var/cache/squid \
    && chown -R squid:squid /var/cache/squid

COPY squid.conf /etc/squid/squid.conf
COPY entrypoint.sh /usr/bin/entrypoint.sh

USER squid

ENTRYPOINT ["squid", "-NYC"]
