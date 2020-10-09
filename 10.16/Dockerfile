ARG NODE_VERSION=10.16
FROM node:$NODE_VERSION-alpine

WORKDIR /app

ENV YARN_VERSION 1.22.4

RUN apk update && \
    apk add --no-cache git g++ make python && \
    apk add --no-cache --virtual .build-deps-yarn curl && \
    curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz" && \
    tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/ && \
    ln -snf /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn && \
    ln -snf /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg && \
    rm yarn-v$YARN_VERSION.tar.gz && \
    apk del .build-deps-yarn && \
    npm config set scripts-prepend-node-path auto && \
    npm config set unsafe-perm true && \
    npm install --global gulp-cli
