FROM ubuntu

RUN apt-get update -y
RUN apt-get install -y proftpd ssh

ADD launch /launch
ADD proftpd.conf /etc/proftpd/proftpd.conf
RUN chown root:root /etc/proftpd/proftpd.conf
RUN mkdir /ftp

EXPOSE 21
EXPOSE 20
EXPOSE 22

ENTRYPOINT /launch

