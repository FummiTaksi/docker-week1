FROM ubuntu:16.04

EXPOSE 8000
COPY . /usr/src/app
WORKDIR /usr/src/app
RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get install -y nodejs
RUN npm install
CMD ["sh", "-c","FRONT_URL=http://localhost:5000 npm start"]