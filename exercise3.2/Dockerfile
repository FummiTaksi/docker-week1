FROM ubuntu:16.04

RUN apt-get update && apt-get install -y python2.7 && \
    apt-get install -y python3-pip && \
    apt-get install -y wget && \
    apt-get install -y ffmpeg && \
    apt-get install -y rtmpdump && \
    pip3 install --user --upgrade yle-dl && \
    export PATH=$PATH:~/.local/bin
CMD ["sh", "-c", "read -p Url: website && sleep 3 && yle-dl $website"]