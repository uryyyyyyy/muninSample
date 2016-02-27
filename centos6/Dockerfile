FROM centos:6
RUN yum update -y && yum clean all

RUN yum -y install yum-priorities wget httpd
RUN wget http://ftp-srv2.kddilabs.jp/Linux/distributions/fedora/epel/6/x86_64/epel-release-6-8.noarch.rpm
RUN rpm -ivh epel-release-6-8.noarch.rpm
RUN yum -y install munin --enablerepo=epel
RUN htpasswd -b /etc/munin/munin-htpasswd admin admin
# RUN service httpd restart
# RUN service munin-node start

CMD /bin/bash
