FROM alpine:3.7

RUN mkdir -p /usr/home/softwares
RUN cd /usr/home/softwares
RUN wget http://apache-mirror.rbc.ru/pub/apache/maven/maven-3/3.3.9/binaries/apache-maven-3.3.9-bin.tar.gz
RUN tar xzvf apache-maven-3.3.9-bin.tar.gz
RUN export PATH=/usr/home/softwares/apache-maven-3.3.9/bin:$PATH
