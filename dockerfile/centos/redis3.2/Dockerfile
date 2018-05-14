FROM centos6-gcc

MAINTAINER bsc2012 "13322808776@189.cn"

RUN yum install -y wget

RUN wget http://download.redis.io/releases/redis-3.2.11.tar.gz

RUN tar xzf redis-3.2.11.tar.gz -C /usr/share/ && rm -rf redis-3.2.11.tar.gz

WORKDIR /usr/share/redis-3.2.11

RUN mkdir conf && cp redis.conf conf/

RUN mkdir data && sed -i 's/dir \.\//dir \/usr\/share\/redis-3.2.11\/data\//g' conf/redis.conf

RUN sed -i 's/bind 127\.0\.0\.1/bind 0\.0\.0\.0/g' conf/redis.conf

RUN ["make"]

ENV REDIS_HOME /usr/share/redis-3.2.11
ENV PATH $PATH:$REDIS_HOME/src

EXPOSE 6379

CMD ["redis-server","conf/redis.conf"]
