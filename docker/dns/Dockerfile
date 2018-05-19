#version 1.0
FROM ubuntu
VOLUME ["~/"]
WORKDIR ~/

RUN apt-get update
RUN echo "test"
RUN apt-get -y install bind9
RUN apt-get -y install dnsutils
RUN rm -v /etc/bind/named.conf.local
ADD config/named.conf.local /etc/bind/
RUN rm -v /etc/bind/db.cuc.edu.cn
ADD config/db.cuc.edu.cn /etc/bind/db.cuc.edu.cn
CMD service bind9 start
