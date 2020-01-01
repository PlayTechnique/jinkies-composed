FROM centos:8

RUN dnf update -y && dnf install -y java-11-openjdk && mkdir /var/jenkins_home/ && groupadd -g 1000 jenkins && useradd -u 1000 -g 1000 jenkins -d /var/jenkins_home && chown jenkins:jenkins /var/jenkins_home

COPY jenkins.war /var/jenkins_home/

ENV JENKINS_HOME /var/jenkins_home
WORKDIR /var/jenkins_home

RUN chown jenkins:jenkins jenkins.war
EXPOSE 8080:8080

USER jenkins
CMD ["java", "-jar", "jenkins.war", "--httpPort=8080"]
