# GlassFish
#
# VERSION 0.1
# DOCKER-VERSION 0.7.0

FROM codenvy/jdk7

RUN sudo apt-get install unzip

#Downloading and unpacking GlassFish 4.0
WORKDIR /opt/
RUN wget download.java.net/glassfish/4.0/release/glassfish-4.0.zip
RUN unzip glassfish-4.0.zip -d /opt
RUN rm glassfish-4.0.zip

#Deleting default web application
RUN rm -rf /opt/glassfish4/glassfish/domains/domain1/autodeploy/*

#open default GlassFish port
EXPOSE 8080
