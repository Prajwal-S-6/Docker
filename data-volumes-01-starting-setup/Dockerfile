FROM node

WORKDIR /volumeapp

COPY package.json .

RUN npm install

COPY . .

EXPOSE 80

#ananymouse volume, doesnt survive container shutdown
#VOLUME ["/volumeapp/feedback"]
#VOLUME ["/volumeapp/node_modules"]

CMD ["node", "server.js"]

#docker run --name volumeapp --rm -d -v my-vol-name:/volumeapp/feedback volumeapp:v1
#docker run --name volumeapp --rm -d -v my-vol-name:/volumeapp/feedback -v "%cd%: /volumeapp" -v /volumeapp/node_modules volumeapp:v1