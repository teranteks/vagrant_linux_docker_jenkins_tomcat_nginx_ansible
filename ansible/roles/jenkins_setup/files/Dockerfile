FROM jenkins/jenkins:lts-jdk11
MAINTAINER Teranteks
USER root
ENV JAVA_OPTS="-Djava.awt.headless=true -Djenkins.install.runSetupWizard=false -Djenkins.model.Jenkins.crumbIssuerProxyCompatibility=true"

#Setup necessary dependencies
RUN apt update
RUN apt-get -y install nano
RUN apt-get -y install git
RUN apt-get -y install ansible

#Setup Jenkins plugins and init script 
COPY --chown=jenkins:jenkins ./jenkins_plugins.txt /usr/share/jenkins/ref/plugins.txt
RUN jenkins-plugin-cli -f /usr/share/jenkins/ref/plugins.txt

COPY --chown=jenkins:jenkins ./initjenkins.groovy /usr/share/jenkins/ref/init.groovy.d/initjenkins.groovy
# Remark: there is no CMD or statement. Since  jenkins/jenkins:lts-jdk11 image uses an ENTRYPOINT, this image will inherit that behavior.

  

