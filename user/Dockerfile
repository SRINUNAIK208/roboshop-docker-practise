FROM node:20-alpine3.23 
WORKDIR /app/server
COPY package.json .
COPY *.js .
RUN npm install
CMD ["node", "server.js"]
