FROM mrbluecorp/centos:7

MAINTAINER wyparks2 <wyparks2@mrblue.com>

ENV JDK_VERSION 11.0.1
ENV JDK_DIR jdk-${JDK_VERSION}
ENV JDK_FILE jdk-${JDK_VERSION}.tar.gz
ENV JAVA_HOME /usr/local/${JDK_DIR}

# JDK 설치
RUN cd /usr/local/src && \
    wget https://download.java.net/java/GA/jdk11/13/GPL/openjdk-11.0.1_linux-x64_bin.tar.gz -O ${JDK_FILE} && \
    tar xzf ${JDK_FILE} && \
    rm -f ${JDK_FILE} && \
    mv ${JDK_DIR} ${JAVA_HOME}

# JAVA_HOME PATH 등록
ENV PATH="$PATH:$JAVA_HOME/bin"
