#version 1.0
FROM ubuntu
VOLUME ["~/"]
WORKDIR ~/

RUN apt-get update
RUN apt-get -y install nfs-kernel-server
RUN mkdir -p /var/nfs/general
RUN chown nobody:nogroup /var/nfs/general
RUN rm /etc/exports
ADD config/exports /etc/exports
CMD service nfs start
