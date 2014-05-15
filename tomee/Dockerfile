# Apache TomEE
#
# VERSION 0.1
# DOCKER-VERSION 0.7.0

FROM sleshchenko/java-7

#Downloading and unpacking TomEE
RUN /usr/bin/sudo /usr/bin/apt-get update
RUN /usr/bin/wget http://apache.rediris.es/openejb/openejb-4.5.1/apache-tomee-1.5.1-webprofile.tar.gz -O /tmp/tomee-1.5.1.tar.gz
RUN mkdir /var/lib/tomee-1.5.1
RUN /bin/tar -xzf /tmp/tomee-1.5.1.tar.gz -C /var/lib/tomee-1.5.1 --strip-components=1
RUN rm /tmp/tomee-1.5.1.tar.gz

#Deleting derafult web application
RUN rm -rf /var/lib/tomee-1.5.1/webapps/*

#open default tomee port
EXPOSE 8080
