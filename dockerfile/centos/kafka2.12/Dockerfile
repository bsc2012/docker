FROM centos6-jdk:8

MAINTAINER bsc2012 "13322808776@189.cn"

RUN yum install -y wget

RUN wget http://mirrors.hust.edu.cn/apache/kafka/1.1.0/kafka_2.12-1.1.0.tgz

RUN tar xzf kafka_2.12-1.1.0.tgz -C /usr/share/ && rm -rf kafka_2.12-1.1.0.tgz

ENV KAFKA_HOME /usr/share/kafka_2.12-1.1.0
ENV PATH $PATH:$KAFKA_HOME/bin

WORKDIR /usr/share/kafka_2.12-1.1.0

EXPOSE 9092

CMD sed -i "s/#advertised\.listeners=PLAINTEXT:\/\/your\.host\.name:9092/advertised\.listeners=PLAINTEXT:\/\/${AD_L:-localhost}:9092/g" config/server.properties \
        && sed -i "s/zookeeper\.connect=localhost:2181/zookeeper\.connect=${ZK_C:-localhost}:2181/g" config/server.properties \
	&& kafka-server-start.sh config/server.properties