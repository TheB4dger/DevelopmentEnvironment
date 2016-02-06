# Jenkins machine
# docker build -t local:jenkins .
# docker run -p 8080:8080 -p 50000:50000 -d local:jenkins
FROM jenkins
MAINTAINER Ben Moorhouse (ben@benslittleoffice.com)

USER root
RUN mkdir /var/log/jenkins && mkdir /var/cache/jenkins
RUN chown -R jenkins:jenkins /var/log/jenkins && chown -R jenkins:jenkins /var/cache/jenkins
USER jenkins

ENV JENKINS_OPTS="--handlerCountStartup=100 --handlerCountMax=300 --logfile=/var/log/jenkins/jenkins.log --webroot=/var/cache/jenkins/war"

EXPOSE 8080 50000
