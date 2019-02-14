FROM docker.io/centos
RUN mkdir -p /opt/app-root
WORKDIR /opt/app-root
USER root
RUN echo "ping google.com -c 3" > testping.sh && echo "uptime" > uptime.sh 
ONBUILD ENTRYPOINT sh /opt/app-root/testping.sh && sh /opt/app-root/uptime.sh 

