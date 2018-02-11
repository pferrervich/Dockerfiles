FROM ubuntu
MAINTAINER pferrervich

RUN apt update -y && apt-get upgrade -y
RUN apt install apache2  -y
RUN apt install ssh -y

ADD index.html /var/www/html/index.html

EXPOSE 80
EXPOSE 22

ENTRYPOINT service apache2 start && bash 
