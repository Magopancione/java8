FROM centos:latest
VOLUME /opt/jboss
VOLUME /home/jboss
RUN yum -y install wget && \
	wget  "https://www.dropbox.com/s/qhi8fi07zmj5dm2/jre-6u45-linux-x64-rpm.bin?dl=0" \
         -O /tmp/jre-6u45-linux-x64-rpm.bin  && \
	chmod a+x /tmp/jre-6u45-linux-x64-rpm.bin && \
    /tmp/jre-6u45-linux-x64-rpm.bin -x && \
    rm /tmp/jre-6u45-linux-x64-rpm.bin && \
    yum -y localinstall /jre-6u45-linux-amd64.rpm && \
    rm /jre-6u45-linux-amd64.rpm

ENV JAVA_HOME /usr/java/default
