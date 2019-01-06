FROM ubuntu:16.04

WORKDIR /mydir 
RUN apt-get update && apt-get install -y curl
CMD ["sh", "-c", "read -p Website: website && sleep 3 && curl http://$website"]