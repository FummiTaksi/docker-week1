FROM ubuntu:16.04

EXPOSE 8000
COPY . /usr/src/app
WORKDIR /usr/src/app
RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get install -y nodejs
RUN npm install
CMD ["sh", "-c","FRONT_URL=http://localhost:5000 REDIS=redis REDIS_PORT=6379 DB_HOST=database DB_USERNAME=possu DB_PASSWORD=password npm start"]