# docker run -p 80:80 --name feedback-app -d --rm
# -v feedback:/app/feedback 
# -v "/Users/diep/Documents/Docker/5-data-volumes/:/app" 
# -v /app/node_modules 
# 91e1c4f67683

FROM node:14

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

EXPOSE 80

CMD [ "npm", "start" ]