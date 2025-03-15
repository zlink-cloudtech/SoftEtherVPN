
FROM homqyy/alpine:3.20.3-CN AS builder
RUN apk add binutils --no-cache \
        linux-headers \
	build-base \
        readline-dev \
        openssl-dev \
        ncurses-dev \
        git \
        cmake \
        zlib-dev \
        libsodium-dev \
        gnu-libiconv

RUN apk add --no-cache \
        vim \
        gdb \
        net-tools \
        tcpdump

ENV LD_PRELOAD=/usr/lib/preloadable_libiconv.so
ENV USE_MUSL=YES
ENV CMAKE_FLAGS="-DSE_PIDDIR=/run/softether -DSE_LOGDIR=/var/log/softether -DSE_DBDIR=/var/lib/softether"