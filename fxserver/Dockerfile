FROM alpine:latest

RUN apk add --no-cache ca-certificates curl rust cargo gcc
RUN apk add --no-cache --upgrade grep

RUN curl -s https://runtime.fivem.net/artifacts/fivem/build_proot_linux/master`curl -s https://runtime.fivem.net/artifacts/fivem/build_proot_linux/master/ | grep 'LATEST RECOMMENDED' -B 1 | grep -Po '(?<=href=".)[^"]*(?=")'` | tar xJ -C /srv
RUN sed -i 's/bash/sh/g' /srv/run.sh
