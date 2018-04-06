FROM node:8-alpine

RUN apk -U add --no-cache python py-pip && \
    pip install --no-cache-dir --upgrade pip awscli && \
    apk --purge -v del py-pip && \
    rm -rf /var/cache/apk/*
