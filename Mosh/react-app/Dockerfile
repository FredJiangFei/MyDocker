FROM node:14.16.0-alpine3.13
RUN addgroup fred && adduser -S -G fred fred
USER fred
WORKDIR /app
COPY . .
RUN npm install
ENV APL_URL=https://jsonplaceholder.typicode.com/
EXPOSE 3000
CMD npm start