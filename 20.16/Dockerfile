ARG NODE_VERSION=20.16
FROM node:$NODE_VERSION-slim

WORKDIR /app

RUN apt update && \
    apt upgrade -y && \
    apt clean