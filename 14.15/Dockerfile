ARG NODE_VERSION=14.15
FROM node:$NODE_VERSION-slim

WORKDIR /app

ENV YARN_VERSION 1.22.10

RUN npm config set scripts-prepend-node-path auto && \
yarn policies set-version $YARN_VERSION && \
npm install --global gulp-cli
