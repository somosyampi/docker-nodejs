ARG NODE_VERSION=12.22
FROM node:$NODE_VERSION-slim

WORKDIR /app

RUN apt update && \
    apt upgrade -y && \
    apt clean && \
    npm config set scripts-prepend-node-path auto && \
    npm config set unsafe-perm true
