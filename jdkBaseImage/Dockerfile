
FROM openjdk:8u265-slim-buster

RUN apt-get update \
   && apt-get install -y vim \
   && apt-get install -y telnet \
   && apt-get install -y iputils-ping

RUN apt-get install -y httpie \
   && apt-get install -y curl

RUN apt-get install -y unzip

RUN apt-get install -y htop

RUN cd /opt && curl https://repo1.maven.org/maven2/com/taobao/arthas/arthas-packaging/3.4.5/arthas-packaging-3.4.5-bin.zip -o arthas.zip 

RUN cd /opt && mkdir arthas && cd arthas && mv ../arthas.zip . && unzip arthas.zip && rm arthas.zip

CMD bash
