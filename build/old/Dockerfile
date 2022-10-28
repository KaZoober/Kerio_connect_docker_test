FROM 	debian:10

COPY kerio-connect-9.4.1-6249-linux-amd64.deb /

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get upgrade -y

RUN apt install -y ./kerio-connect-9.4.1-6249-linux-amd64.deb

CMD service kerio-connect start && tail -f /opt/kerio/mailserver/store/logs/debug.log