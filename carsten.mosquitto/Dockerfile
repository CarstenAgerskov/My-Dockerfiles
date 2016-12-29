FROM ubuntu:16.04

MAINTAINER carsten 

RUN apt-get update && apt-get install -y \
        wget \
	mosquitto

COPY etc/mosquitto/conf.d/ /etc/mosquitto/conf.d/

EXPOSE 1883 9001
CMD /usr/sbin/mosquitto -c /etc/mosquitto/mosquitto.conf
