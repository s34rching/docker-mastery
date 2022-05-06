FROM node:18-alpine

EXPOSE 8080 3000

RUN apk add --no-cache tini

RUN mkdir -p /usr/src/app

WORKDIR /usr/src/app

COPY package.json package.json

RUN npm install \
    && npm cache clean --force

COPY . .

CMD ["/sbin/tini", "--", "node", "./bin/www"]

# use this empty Dockerfile to build your assignment

# NOTE: The instructions are now in the README.md file in this directory.
