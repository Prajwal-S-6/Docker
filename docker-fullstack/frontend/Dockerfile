FROM node

WORKDIR /multi-app/frontend

COPY  package.json .

RUN npm install

COPY . .

EXPOSE 3000

CMD ["npm", "start"]