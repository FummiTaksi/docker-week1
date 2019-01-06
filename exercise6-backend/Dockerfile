FROM ubuntu:16.04

EXPOSE 8000
COPY . /usr/src/app
WORKDIR /usr/src/app
RUN apt-get update && apt-get install -y curl && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt-get install -y nodejs && \
    npm install && rm -rf /var/lib/apt/lists/* && \
    useradd -m app && \
    chown -R app /usr/src/app
USER app
WORKDIR app
CMD ["sh", "-c","FRONT_URL=http://localhost:5000 REDIS=redis REDIS_PORT=6379 DB_HOST=database DB_USERNAME=possu DB_PASSWORD=password npm start"]