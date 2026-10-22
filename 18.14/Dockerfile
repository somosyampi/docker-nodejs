ARG NODE_VERSION=18.14
FROM node:$NODE_VERSION-slim

WORKDIR /app

RUN sed -i -e 's|deb.debian.org|archive.debian.org|g' /etc/apt/sources.list

RUN apt update && \
    apt upgrade -y && \
    apt clean