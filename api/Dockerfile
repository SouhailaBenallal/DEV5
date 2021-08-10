FROM node:15

WORKDIR /app

COPY ./ ./

RUN npm install
RUN npm run build
RUN npm run migrate:latest
RUN npm run test

CMD ["npm", "start"]
