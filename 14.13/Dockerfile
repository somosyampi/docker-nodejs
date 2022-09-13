ARG NODE_VERSION=14.13
FROM node:$NODE_VERSION-alpine

WORKDIR /app

ENV YARN_VERSION 1.22.4

RUN apk update
RUN apk add --no-cache git g++ make python
RUN apk add --no-cache --virtual .build-deps-yarn curl
RUN curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"
RUN tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/
RUN ln -snf /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn
RUN ln -snf /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg
RUN rm yarn-v$YARN_VERSION.tar.gz
RUN apk del .build-deps-yarn
RUN npm config set scripts-prepend-node-path auto
RUN npm install --global gulp-cli
