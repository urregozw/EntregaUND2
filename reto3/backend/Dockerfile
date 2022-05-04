FROM node:14-alpine

COPY *.json ./

RUN npm install

COPY . ./

CMD ["node", "server.js"]
