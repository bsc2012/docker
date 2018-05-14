FROM centos:6

MAINTAINER bsc2012 "13322808776@189.cn"


RUN yum install -y wget

RUN wget --no-check-certificate --no-cookies --header "Cookie: oraclelicense=accept-securebackup-cookie" http://download.oracle.com/otn-pub/java/jdk/8u171-b11/512cd62ec5174c3487ac17c61aaa89e8/jdk-8u171-linux-x64.tar.gz

RUN tar xzf jdk-8u171-linux-x64.tar.gz -C /usr/share/ && rm -rf jdk-8u171-linux-x64.tar.gz

ENV JAVA_HOME /usr/share/jdk1.8.0_171
ENV PATH $PATH:$JAVA_HOME/bin
