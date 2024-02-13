FROM node:14

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

EXPOSE 80

# anonymous volume, will be deleted upon container restart
VOLUME [ "/app/feedback" ]

CMD [ "node", "server.js" ]