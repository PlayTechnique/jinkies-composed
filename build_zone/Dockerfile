FROM centos:8

RUN dnf update -y && dnf install -y java-11-openjdk && mkdir /var/jenkins_home/
COPY jenkins.war /var/jenkins_home/

