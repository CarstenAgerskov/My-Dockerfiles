FROM ubuntu:16.04

MAINTAINER Carsten

RUN apt-get update && apt-get install -y \
	software-properties-common 


RUN echo oracle-java8-installer shared/accepted-oracle-license-v1-1 select true | debconf-set-selections && \
  add-apt-repository -y ppa:webupd8team/java && \
  apt-get update && apt-get install -y \
	oracle-java8-installer \
        wget \
	unzip

RUN rm -rf /var/cache/oracle-jdk8-installer

RUN wget https://openhab.ci.cloudbees.com/job/openHAB-Distribution/lastSuccessfulBuild/artifact/distributions/openhab-offline/target/openhab-offline-2.0.0-SNAPSHOT.zip
RUN cd /opt && mkdir openhab && cd openhab && unzip /openhab-offline-2.0.0-SNAPSHOT.zip

EXPOSE 8080
CMD /opt/openhab/start_debug.sh



