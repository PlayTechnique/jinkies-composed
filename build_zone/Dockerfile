FROM centos:8

ENV JENKINS_HOME /var/jenkins_home

RUN dnf update -y && dnf install -y java-11-openjdk && mkdir ${JENKINS_HOME}/ && groupadd -g 1000 jenkins && useradd -u 1000 -g 1000 jenkins -d ${JENKINS_HOME} && chown jenkins:jenkins ${JENKINS_HOME}

COPY jenkins.war ${JENKINS_HOME}/

WORKDIR ${JENKINS_HOME}

RUN chown jenkins:jenkins jenkins.war
EXPOSE 8080:8080

USER jenkins
CMD ["java", "-Djenkins.install.runSetupWizard=false", "-jar", "jenkins.war", "--httpPort=8080"]
