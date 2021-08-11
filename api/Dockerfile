FROM node:15

WORKDIR /app

COPY ./ ./

RUN npm install
RUN npm run build
RUN npx knex migrate:latest --knexfile dist/db/knexfile.js 
RUN npm run test

CMD ["npm", "start"]
