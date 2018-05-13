FROM centos6-gcc

MAINTAINER bas2012 "13322808776@189.cn"

RUN yum install -y wget

RUN wget http://download.redis.io/releases/redis-3.2.11.tar.gz

RUN tar xzf redis-3.2.11.tar.gz -C /usr/share/ && rm -rf redis-3.2.11.tar.gz

WORKDIR /usr/share/redis-3.2.11

RUN ["make"]

ENV REDIS_HOME /usr/share/redis-3.2.11
ENV PATH $PATH:$REDIS_HOME/src

EXPOSE 6379

CMD ["redis-server"]