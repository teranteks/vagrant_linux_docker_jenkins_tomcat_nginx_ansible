# FROM jenkins/jenkins:lts-jdk11
# MAINTAINER Teranteks

# #ENV JAVA_ARGS="-Djava.awt.headless=true -Djenkins.install.runSetupWizard=false -Djenkins.model.Jenkins.crumbIssuerProxyCompatibility=true"
# ENV JAVA_OPTS="-Djenkins.install.runSetupWizard=false"

# COPY --chown=jenkins:jenkins /tmp/jenkins/build-dockerfile/jenkins_plugins.txt /usr/share/jenkins/ref/plugins.txt
# RUN jenkins-plugin-cli -f /usr/share/jenkins/ref/plugins.txt
# COPY --chown=jenkins:jenkins ./initjenkins.groovy /usr/share/jenkins/ref/init.groovy.d/initjenkins.groovy
# # Remark: there is no CMD or statement. Since  jenkins/jenkins:lts-jdk11 image uses an ENTRYPOINT, this image will inherit that behavior.

FROM jenkins/jenkins:lts-jdk11
MAINTAINER Teranteks

ENV JAVA_OPTS="-Djava.awt.headless=true -Djenkins.install.runSetupWizard=false -Djenkins.model.Jenkins.crumbIssuerProxyCompatibility=true"

  
COPY --chown=jenkins:jenkins ./jenkins_plugins.txt /usr/share/jenkins/ref/plugins.txt
RUN jenkins-plugin-cli -f /usr/share/jenkins/ref/plugins.txt

COPY --chown=jenkins:jenkins ./initjenkins.groovy /usr/share/jenkins/ref/init.groovy.d/initjenkins.groovy
# Remark: there is no CMD or statement. Since  jenkins/jenkins:lts-jdk11 image uses an ENTRYPOINT, this image will inherit that behavior.


  

