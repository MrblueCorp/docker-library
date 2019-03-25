FROM mrbluecorp/centos:7

MAINTAINER wyparks2 <wyparks2@mrblue.com>

ENV JDK_VERSION 1.8.202
ENV JDK_DIR jdk-${JDK_VERSION}
ENV JDK_FILE jdk-${JDK_VERSION}.tar.gz
ENV JAVA_HOME /usr/local/${JDK_DIR}

ENV DOWNLOAD_URL https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u202-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u202b08.tar.gz
ENV UNARCHIVE_DIR_NAME jdk8u202-b08

# JDK 설치
RUN cd /usr/local/src && \
    wget ${DOWNLOAD_URL} -O ${JDK_FILE} && \
    tar xzf ${JDK_FILE} && \
    mv ${UNARCHIVE_DIR_NAME} ${JDK_DIR} && \
    rm -f ${JDK_FILE} && \
    mv ${JDK_DIR} ${JAVA_HOME}

# JAVA_HOME PATH 등록
ENV PATH="$PATH:$JAVA_HOME/bin"