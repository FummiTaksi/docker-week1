FROM ubuntu:16.04

EXPOSE 5000
COPY . /usr/src/app
WORKDIR /usr/src/app
RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get install -y nodejs
RUN npm install
RUN npm build
CMD ["sh", "-c", "API_URL=http://localhost:8000 npm start"]