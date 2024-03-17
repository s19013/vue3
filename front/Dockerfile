# from node:18-alpine
FROM node:18-slim
WORKDIR /app
COPY . /app
# alpineでは apt,apt-getは使えない,apk,apk-addを使うらしい｡
# RUN apk update
run apt-get update
run yarn install
# run npm install
CMD ["yarn", "dev"]
