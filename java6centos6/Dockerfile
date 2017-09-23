FROM centos:centos6
VOLUME /opt/jboss
VOLUME /home/jboss
RUN yum -y install wget && \
	wget --no-cookies \
         --no-check-certificate \
         --header "Cookie: oraclelicense=accept-securebackup-cookie" \
         "http://download.oracle.com/otn-pub/java/jdk/6u45-b06/jre-6u45-linux-x64-rpm.bin" \
         -O /tmp/jre-6u45-linux-x64-rpm.bin  && \
	chmod a+x /tmp/jre-6u45-linux-x64-rpm.bin && \
    /tmp/jre-6u45-linux-x64-rpm.bin -x && \
    rm /tmp/jre-6u45-linux-x64-rpm.bin && \
    yum -y localinstall /jre-6u45-linux-amd64.rpm && \
    rm /jre-6u45-linux-amd64.rpm && \
    yum clean all

ENV JAVA_HOME /usr/java/default
