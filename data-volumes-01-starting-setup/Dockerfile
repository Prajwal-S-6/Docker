FROM node

WORKDIR /volumeapp

COPY package.json .

RUN npm install

COPY . .

ARG DEFAULT_PORT=80

ENV PORT $DEFAULT_PORT

EXPOSE $PORT

#ananymouse volume, doesnt survive container shutdown
#VOLUME ["/volumeapp/feedback"]
#VOLUME ["/volumeapp/node_modules"]

CMD ["node", "server.js"]

#docker run --name volumeapp --rm -d -v my-vol-name:/volumeapp/feedback volumeapp:v1
#docker run --name volumeapp --rm -d -v my-vol-name:/volumeapp/feedback -v "%cd%: /volumeapp" -v /volumeapp/node_modules volumeapp:v1
#docker run --name volumeapp --rm -d -e PORT=8000 -v my-vol-name:/volumeapp/feedback -v "%cd%: /volumeapp" -v /volumeapp/node_modules volumeapp:v1
#docker run --name volumeapp --rm -d --env-file .env -v my-vol-name:/volumeapp/feedback -v "%cd%: /volumeapp" -v /volumeapp/node_modules volumeapp:v1