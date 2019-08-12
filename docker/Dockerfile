FROM node:8-alpine

COPY package.json package.json
RUN  npm install

USER root
COPY . .

RUN  chown -R app:appgrp .
USER app

CMD npm start
