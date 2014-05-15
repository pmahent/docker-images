# JBoss
#
# VERSION 0.1
# DOCKER-VERSION 0.7.0

FROM sleshchenko/java-7

#Downloading and unpacking JBoss
RUN apt-get update
RUN wget http://download.jboss.org/jbossas/7.1/jboss-as-7.1.1.Final/jboss-as-7.1.1.Final.tar.gz -O /tmp/jboss7.tar.gz
RUN mkdir /opt/jboss7
RUN tar -xzf /tmp/jboss7.tar.gz -C /opt/jboss7 --strip-components=1
RUN rm /tmp/jboss7.tar.gz

#Set default configuration
WORKDIR /opt/jboss7/standalone/configuration/
RUN sed -i 's/enable-welcome-root="true"/enable-welcome-root="false"/g' standalone.xml
RUN sed -i 's/127.0.0.1/0.0.0.0/g' standalone.xml

#open default jboss port
EXPOSE 8080
