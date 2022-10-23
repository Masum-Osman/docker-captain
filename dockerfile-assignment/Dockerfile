FROM node:18-alpine3.15
EXPOSE 3000
RUN apk add --update tini
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app
COPY package.json package.json
RUN npm install && npm cache  clean
COPY . .
CMD ["tini", "--", "node", "./bin/www"]
