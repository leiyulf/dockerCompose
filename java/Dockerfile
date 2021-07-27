# Version 0.0.1
FROM ubuntu:latest
MAINTAINER leiyu "18068064015"

ENV REFRESHED_AT 2021-7-19

RUN mkdir /usr/local/lib/java8

ADD jdk-8u291-linux-x64.tar.gz /usr/local/lib/java8


ENV JAVA_HOME /usr/local/lib/java8/jdk1.8.0_291
ENV JRE_HOME $JAVA_HOME/jre
ENV CLASSPATH .:$JAVA_HOME/lib:$JRE_HOME/lib
ENV PATH $JAVA_HOME/bin:$JRE_HOME/bin:$PATH

#RUN /usr/bin/bash -c "source /etc/profile"

RUN mkdir -p /usr/local/jar
ADD $PWD/jar /usr/local/jar
WORKDIR /usr/local/jar

EXPOSE 6060

CMD java -jar test.jar
