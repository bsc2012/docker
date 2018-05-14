FROM centos6-jdk:8

MAINTAINER bsc2012 "13322808776@189.cn"

RUN yum install -y wget

RUN wget http://mirrors.shu.edu.cn/apache/zookeeper/zookeeper-3.4.12/zookeeper-3.4.12.tar.gz

RUN tar xzf zookeeper-3.4.12.tar.gz -C /usr/share/ && rm -rf zookeeper-3.4.12.tar.gz

ENV ZOOKEEPER_HOME /usr/share/zookeeper-3.4.12
ENV PATH $PATH:$ZOOKEEPER_HOME/bin

RUN cp /usr/share/zookeeper-3.4.12/conf/zoo_sample.cfg /usr/share/zookeeper-3.4.12/conf/zoo.cfg

EXPOSE 2181

CMD zkServer.sh start-foreground
