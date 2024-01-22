ARG NODE_VERSION=12.22
FROM node:$NODE_VERSION-stretch

WORKDIR /app

RUN sed -i -e 's/deb.debian.org/archive.debian.org/g' \
           -e 's|security.debian.org|archive.debian.org/|g' \
           -e '/stretch-updates/d' /etc/apt/sources.list

RUN apt update && \
    apt upgrade -y && \
    apt clean && \
    npm config set scripts-prepend-node-path auto && \
    npm config set unsafe-perm true
