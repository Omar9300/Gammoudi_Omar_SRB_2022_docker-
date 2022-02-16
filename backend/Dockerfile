FROM node:10-alpine

WORKDIR /usr/src/app

COPY package*.json ./

COPY . .

RUN npm install

EXPOSE 8001

CMD ["node", "server.js"]
