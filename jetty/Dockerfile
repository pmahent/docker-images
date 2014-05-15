# Jetty
#
# VERSION 0.1
# DOCKER-VERSION 0.7.0

FROM ubuntu
# make sure the package repository is up to date
RUN apt-get install -y software-properties-common
RUN add-apt-repository ppa:webupd8team/java
RUN apt-get update

# automatically accept oracle license
RUN echo oracle-java7-installer shared/accepted-oracle-license-v1-1 select true | /usr/bin/debconf-set-selections
# and install java 7 oracle jdk
RUN apt-get -y install oracle-java7-installer && apt-get clean
RUN update-alternatives --display java
RUN echo "JAVA_HOME=/usr/lib/jvm/java-7-oracle" >> /etc/environment

#Downloading and unpacking Jetty
RUN /usr/bin/sudo /usr/bin/apt-get update
RUN /usr/bin/wget http://saimei.acc.umu.se/mirror/eclipse.org/jetty/stable-9/dist/jetty-distribution-9.1.5.v20140505.tar.gz -O /tmp/jetty9.tar.gz
RUN mkdir /var/lib/jetty9
RUN /bin/tar -xzf /tmp/jetty9.tar.gz -C /var/lib/jetty9 --strip-components=1
RUN rm /tmp/jetty9.tar.gz
RUN cp /var/lib/jetty9/bin/jetty.sh /etc/init.d/jetty
RUN echo JETTY_HOME='/var/lib/jetty9' > /etc/default/jetty

#open default jetty port
EXPOSE 8080
