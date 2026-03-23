FROM node

WORKDIR /backendApp

COPY package.json .

RUN npm install

COPY . .

EXPOSE 80

ENV MONGODB_USERNAME=root

ENV MONGODB_PASSWORD=password

CMD ["node", "app.js"]

# docker run --rm -d --name mongo-db -v mongo-data:/data/db --network multi-app --env-file .env mongo
# docker run --name backend --rm -d -v logs:/backendApp/logs -v "$(PWD):/backendApp" -v /backendApp/node_modules --network multi-app -p 8080:80 -e MONGODB_USERNAME=praj backend:v1
# docker run --name frontend -d --rm -p 3000:3000 frontend:v1