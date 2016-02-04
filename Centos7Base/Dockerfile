# This just takes the latest from the CentOS guys and runs any updates needed
FROM centos:7
MAINTAINER Ben Moorhouse (ben@benslittleoffice.com)

RUN yum -y update 

CMD ["/bin/bash"]

# docker build -t local:centos7base .
# docker run -ti --name centos7base local:centos7base /bin/bash