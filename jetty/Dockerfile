# Jetty
#
# VERSION 0.1
# DOCKER-VERSION 0.7.0

FROM codenvy/jdk

#Downloading and unpacking Jetty
RUN /usr/bin/sudo /usr/bin/apt-get update
RUN /usr/bin/wget http://saimei.acc.umu.se/mirror/eclipse.org/jetty/stable-9/dist/jetty-distribution-9.1.5.v20140505.tar.gz -O /tmp/jetty9.tar.gz
RUN mkdir /opt/jetty9
RUN /bin/tar -xzf /tmp/jetty9.tar.gz -C /opt/jetty9 --strip-components=1
RUN rm /tmp/jetty9.tar.gz

#open default jetty port
EXPOSE 8080
