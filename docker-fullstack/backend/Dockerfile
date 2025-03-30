FROM node

WORKDIR /multi-app/backend

COPY package.json .

RUN npm install

COPY . .

EXPOSE 80

ENV MONGODB_USERNAME=admin
ENV MONGODB_PASSWORD=password

CMD ["npm", "start"]
