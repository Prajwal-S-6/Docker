FROM node

WORKDIR /volumeapp

COPY package.json .

RUN npm install

COPY . .

EXPOSE 80

#ananymouse volume, doesnt survive container shutdown
#VOLUME ["/volumeapp/feedback"]

CMD ["node", "server.js"]

#docker run --name volumeapp --rm -d -v my-vol-name:/volumeapp/feedback volumeapp:v1