FROM ubuntu:14.04

ENV HOME /root
WORKDIR /root

RUN apt-get update
RUN apt-get install build-essential bison flex automake autoconf libtool make nodejs git expect -y
RUN git clone https://github.com/thiagoralves/OpenPLC_v2.git

WORKDIR /root/OpenPLC_v2

ADD expect_install .
RUN chmod +x expect_install
RUN ls
RUN ./expect_install

RUN apt-get clean

EXPOSE 8080
ENTRYPOINT ["/usr/bin/nodejs", "server.js"]
