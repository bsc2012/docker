FROM centos:6

MAINTAINER bsc2012 "13322808776@189.cn"

RUN yum install -y wget

RUN wget https://archive.apache.org/dist/zookeeper/zookeeper-3.4.12/zookeeper-3.4.12.tar.gz

RUN tar xzf zookeeper-3.4.12.tar.gz -C /usr/share/ && rm -rf zookeeper-3.4.12.tar.gz

ENV ZOOKEEPER_HOME /user/share/zookeeper-3.4.12
ENV PATH $PATH:ZOOKEEPER_HOME/bin

EXPOSE 2181

CMD zkServer.sh start-foreground