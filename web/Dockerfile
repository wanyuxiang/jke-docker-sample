FROM java:7-jdk 
MAINTAINER wanyux

# Install JKE
COPY jke.zip /opt/jke/
RUN unzip /opt/jke/jke*.zip
RUN chmod u+x *.sh
#CMD ./jke.server.linux.sh restart 
#&& tail -F /var/log/faillog
