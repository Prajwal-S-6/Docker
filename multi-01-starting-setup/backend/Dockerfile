FROM node

WORKDIR /backendApp

COPY package.json .

RUN npm install

COPY . .

EXPOSE 80

CMD ["node", "app.js"]

# docker run --rm -d --name mongo-db -v mongo-data:/data/db --network multi-app mongo
# docker run --name backend -d --rm --network multi-app -p 8080:80 backend:v1
# docker run --name frontend -d --rm -p 3000:3000 frontend:v1