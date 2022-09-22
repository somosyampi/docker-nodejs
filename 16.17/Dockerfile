ARG NODE_VERSION=16.17
FROM node:$NODE_VERSION-slim

WORKDIR /app

ENV YARN_VERSION 1.22.10

RUN npm config set scripts-prepend-node-path auto && \
yarn policies set-version $YARN_VERSION && \
npm install --global gulp-cli
