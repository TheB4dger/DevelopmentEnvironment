## Nginx as Reverse Proxy

FROM centos:7
MAINTAINER Ben Moorhouse (ben@benslittleoffice.com)

# Update the system and install Nginx
RUN yum -y update; yum clean all
RUN yum -y install http://nginx.org/packages/centos/7/noarch/RPMS/nginx-release-centos-7-0.el7.ngx.noarch.rpm; yum -y makecache
RUN yum -y install nginx-1.8.0; yum clean all

# Remove some default stuff that we dont need
RUN rm /etc/nginx/conf.d/default.conf
RUN rm /etc/nginx/conf.d/example_ssl.conf

# Load our configuration files
COPY conf/jenkins.conf /etc/nginx/conf.d/jenkins.conf
COPY conf/nginx.conf /etc/nginx/nginx.conf

# Nginx uses port 80
EXPOSE 80

# start nginx
CMD ["nginx"]