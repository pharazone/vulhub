FROM debian:jessie

MAINTAINER phithon <root@leavesongs.com>

RUN apt-get update \
    && apt-get install -y build-essential wget autoconf \
    && cd /usr/src \
    && wget -qO- https://download.samba.org/pub/rsync/src/rsync-2.6.9.tar.gz \
        | tar zx -C /usr/src --strip-components=1 \
    && ./configure \
    && make && make install \
    && apt-get purge -y --auto-remove build-essential wget autoconf \
    && rm -rf /usr/src/* /var/lib/apt/lists/*