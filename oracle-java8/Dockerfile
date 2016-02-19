#
# Oracle Java 8 Dockerfile
#
# https://github.com/dockerfile/java
# https://github.com/dockerfile/java/tree/master/oracle-java8
#

# Pull base image.
FROM ubuntu:14.04

# Install Java.
RUN apt-get update
RUN apt-get install software-properties-common -y
RUN add-apt-repository -y ppa:webupd8team/java 
RUN apt-get update 
RUN echo oracle-java8-installer shared/accepted-oracle-license-v1-1 select true | sudo /usr/bin/debconf-set-selections
RUN apt-get install -y oracle-java8-installer 
RUN rm -rf /var/lib/apt/lists/* 
RUN rm -rf /var/cache/oracle-jdk8-installer


# Define working directory.
WORKDIR /data

# Define commonly used JAVA_HOME variable
ENV JAVA_HOME /usr/lib/jvm/java-8-oracle

# Define default command.
CMD ["bash"]
