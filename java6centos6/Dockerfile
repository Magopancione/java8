FROM centos:centos6
VOLUME /opt/jboss
VOLUME /home/jboss
ADD ./jre-6u45-linux-x64-rpm.bin /tmp/jre-6u45-linux-x64-rpm.bin
RUN chmod a+x /tmp/jre-6u45-linux-x64-rpm.bin && \
    /tmp/jre-6u45-linux-x64-rpm.bin -x && \
    rm /tmp/jre-6u45-linux-x64-rpm.bin && \
    yum -y localinstall /jre-6u45-linux-amd64.rpm && \
    rm /jre-6u45-linux-amd64.rpm

ENV JAVA_HOME /usr/java/default
