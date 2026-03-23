FROM node

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

CMD ["node", "app.js"]

#docker network create my_network
#docker run --rm --name networks --network my_network networks:v1
#docker run --rm --name mongo-db --network my_network mongo
#host.docker.internal
#container name: http://mongo-db/...