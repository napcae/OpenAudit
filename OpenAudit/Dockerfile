# A basic apache server. To use either add or bind mount content under /var/www
FROM ubuntu:14.04

MAINTAINER Chi Trung Nguyen version: 0.1

ADD OAE-Linux-x86_64-release_1.12.8.2.run /tmp/OAE-Linux-x86_64-release_1.12.8.2.run

RUN chmod +x /tmp/OAE-Linux-x86_64-release_1.12.8.2.run
RUN apt-get update && apt-get install -y apache2 apache2-utils libapache2-mod-proxy-html libapache2-mod-php5 openssh-client php5 php5-ldap php5-mcrypt php5-mysql php5-snmp nmap zip wget curl sshpass screen smbclient libtime-modules-perl ipmitool

RUN /tmp/OAE-Linux-x86_64-release_1.12.8.2.run --noexec

ENTRYPOINT ["bash"]

EXPOSE 80