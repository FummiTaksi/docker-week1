FROM ubuntu:16.04

EXPOSE 5000
COPY . /usr/src/app
WORKDIR /usr/src/app
RUN apt-get update && apt-get install -y curl && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt-get install -y nodejs && \
    npm install && npm build && \
    rm -rf /var/lib/apt/lists/* && \
    useradd -m app && \
    chown -R app /usr/src/app
USER app
WORKDIR app
CMD ["sh", "-c", "API_URL=http://localhost:8000 npm start"]