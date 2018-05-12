FROM centos6-jdk:8

MAINTAINER bsc2012 "13322808776@189.cn"

RUN wget http://mirrors.tuna.tsinghua.edu.cn/apache/tomcat/tomcat-8/v8.5.31/bin/apache-tomcat-8.5.31.tar.gz

RUN tar xzf apache-tomcat-8.5.31.tar.gz -C /usr/share/ && rm -rf apache-tomcat-8.5.31.tar.gz

ENV CATALINA_HOME /usr/share/apache-tomcat-8.5.31

ENV PATH $PATH:$CATALINA_HOME/bin

EXPOSE 8080

CMD /usr/share/apache-tomcat-8.5.31/bin/startup.sh && tail -f /usr/share/apache-tomcat-8.5.31/logs/catalina.out
