FROM node:15.14-slim

WORKDIR /app

COPY app/package*.json ./

RUN yarn install && yarn cache clean

COPY app .
