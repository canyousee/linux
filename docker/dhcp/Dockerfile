#version 1.0
FROM ubuntu
VOLUME ["~/"]
WORKDIR ~/

RUN apt-get update
RUN apt-get -y install isc-dhcp-server
RUN rm -v /etc/network/interfaces
RUN rm -v /etc/default/isc-dhcp-server
RUN rm -v /etc/dhcp/dhcpd.conf
ADD config/interfaces /etc/network/interfaces
ADD config/isc-dhcp-server /etc/default/isc-dhcp-server
ADD config/dhcpd.conf /etc/dhcp/dhcpd.conf
CMD service dhcp start
