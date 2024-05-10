#Using Node.js 14 Image
FROM node:14
WORKDIR /app
COPY package*.json ./
#Install dependencies
RUN npm install
COPY . .
EXPOSE 3000
CMD [ "node","app.js" ]
