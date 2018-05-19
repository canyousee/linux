#version 1.0
FROM ubuntu
VOLUME ["~/"]
WORKDIR ~/

RUN apt-get update
RUN apt-get -y install samba
RUN useradd -M -s /sbin/nologin smbuser
RUN rm -v /etc/samba/smb.conf
ADD config/smb.conf /etc/samba/
RUN groupadd smbgroup
RUN usermod -G smbgroup smbuser
RUN mkdir -p /home/samba/guest/
RUN mkdir -p /home/samba/demo/
RUN chgrp -R smbgroup /home/samba/guest/
RUN chgrp -R smbgroup /home/samba/demo/
RUN chmod 2775 /home/samba/guest/
RUN chmod 2770 /home/samba/demo/
CMD service samba start
