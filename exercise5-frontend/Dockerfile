FROM node:alpine

EXPOSE 5000
COPY . /usr/src/app
WORKDIR /usr/src/app
RUN npm install && npm build && \
    rm -rf /var/lib/apt/lists/* && \
    adduser -D app && \
    chown -R app /usr/src/app
USER app
WORKDIR app
CMD ["sh", "-c", "API_URL=http://localhost:8000 npm start"]