ARG NODE_VERSION=24.15
FROM node:$NODE_VERSION-slim

WORKDIR /app

RUN apt update && \
    apt upgrade -y && \
    apt clean && \
    npm install -g pnpm
