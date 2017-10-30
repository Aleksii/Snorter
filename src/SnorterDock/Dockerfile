#Kali docker with SNORT + BARNYARD2 + PULLEDPORK
#Version 0.1.0
From kalilinux/kali-linux-docker:latest
MAINTAINER Joan Bono <@joan_bono>


ENV OINKCODE="***"
ENV INTERFACE="eth0"

RUN apt-get update && apt-get install -y git curl wget
RUN git clone https://github.com/Aleksii/Snorter.git /opt/Snorter
RUN chmod 755 /opt/Snorter/src/Snorter.sh
RUN sed -i "s/sudo //g" /opt/Snorter/src/Snorter
USER root
WORKDIR /opt/Snorter
CMD /opt/Snorter/src/Snorter.sh -o ${OINKCODE} -i ${INTERFACE}


