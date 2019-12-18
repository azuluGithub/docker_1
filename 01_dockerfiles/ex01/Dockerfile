FROM debian

ENV TS3SERVER_LICENSE=accept

WORKDIR /home/teamspeak

EXPOSE 9987/udp 10011 30033

RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y wget bzip2 && \
    wget http://dl.4players.de/ts/releases/3.0.13.4/teamspeak3-server_linux_amd64-3.0.13.4.tar.bz2 && \
    tar -xvf teamspeak3-server_linux_amd64-3.0.13.4.tar.bz2

WORKDIR teamspeak3-server_linux_amd64

ENTRYPOINT sh ts3server_minimal_runscript.sh

#---------------------------------------- REF -----------------------------------
# docker build -t ex01 .
# docker run -it -p 9987:9987/udp -p 30033:30033 -p 10011:10011 ex01
#https://unixblogger.com/setup-a-teamspeak-3-server-on-linux-ubuntu-debian/
#https://www.hostinger.com/tutorials/how-to-make-a-teamspeak-3-server/
#--------------------------------------------------------------------------------
