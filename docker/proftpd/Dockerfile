#version 1.0
FROM ubuntu
VOLUME ["~/"]
WORKDIR ~/

RUN apt-get update
RUN echo "test"
RUN apt-get -y install proftpd
RUN rm -v /etc/proftpd/proftpd.conf
ADD docker/proftpd/config/proftpd.conf /etc/proftpd/
CMD service proftpd start
