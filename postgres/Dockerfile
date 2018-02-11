FROM linuxserver/duplicati
MAINTAINER pferrervich

RUN apt update && apt upgrade -y
RUN apt install -y sudo vim ssh postgresql

ADD sshd_config /etc/ssh/

RUN echo "root:123" | chpasswd

EXPOSE 8200

ENTRYPOINT service ssh start && service postgresql start && mono /app/duplicati/Duplicati.Server.exe --webservice-interface=any --server-datafolder=/config  && bash 
