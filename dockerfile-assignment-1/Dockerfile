FROM node:6-alpine

# EXPOSE 80

RUN apk add --no-cache tini

WORKDIR /usr/src/app

COPY package.json ./

RUN npm install && npm cache clean --force

COPY . ./

CMD ["/sbin/tini", "--", "node", "./bin/www"]