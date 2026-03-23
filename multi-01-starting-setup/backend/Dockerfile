FROM node

WORKDIR /backendApp

COPY package.json .

RUN npm install

COPY . .

EXPOSE 80

CMD ["node", "app.js"]