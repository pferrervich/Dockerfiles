FROM ubuntu
VOLUME /data
EXPOSE 8080
ENV ACTIVE_PROFILE=docker

ENV DL_LINK=https://github.com/streamaserver/streama/releases/download/v1.6.1/streama-1.6.1.war

RUN apt-get update && apt-get install -y openjdk-8-jdk wget 

WORKDIR /app

RUN wget $DL_LINK -O streama.war

ENTRYPOINT /bin/sh -c "java -Dgrails.env=$ACTIVE_PROFILE -jar streama.war"

