# Ex8:docker install proftpd,samba,nfs,dhcp,dns #

## 一、docker 安装 ##

安装docker主程序
![](image/1.PNG)
![](image/2.PNG)
![](image/3.PNG)

加速访问docker hub
![](image/4.PNG)

参考：[https://docs.docker.com/install/linux/docker-ce/ubuntu/](https://docs.docker.com/install/linux/docker-ce/ubuntu/)

## 二、一键部署 ##

ftp

	 sudo docker build -t proftpd:1.0 -f Dockerfile .

![](image/5.PNG)

nfs

	 sudo docker build -t nfs:1.0 -f Dockerfile .

![](image/6.PNG)

samba

	 sudo docker build -t samba:1.0 -f Dockerfile .

![](image/8.PNG)	
![](image/9.PNG)
dhcp

	 sudo docker build -t dhcp:1.0 -f Dockerfile .

![](image/10.PNG)

dns

	sudo docker build -t dns:1.0 -f Dockerfile .

![](image/11.PNG)


