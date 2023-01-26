FROM node

WORKDIR /app

COPY package*.json /app/

RUN npm ci --only=production && npm audit fix

COPY . /app/

EXPOSE 8080

ENV DEBUG=True

ENTRYPOINT [ "node", "server.js" ]
