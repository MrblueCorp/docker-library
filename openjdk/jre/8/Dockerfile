FROM mrbluecorp/centos:7

MAINTAINER wyparks2 <wyparks2@mrblue.com>

ENV JRE_VERSION 1.8.202
ENV JRE_DIR jre-${JRE_VERSION}
ENV JRE_FILE jre-${JRE_VERSION}.tar.gz
ENV JAVA_HOME /usr/local/${JRE_DIR}

ENV DOWNLOAD_URL https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u202-b08/OpenJDK8U-jre_x64_linux_hotspot_8u202b08.tar.gz
ENV UNARCHIVE_DIR_NAME jdk8u202-b08-jre

# JRE 설치
RUN cd /usr/local/src && \
    wget ${DOWNLOAD_URL} -O ${JRE_FILE} && \
    tar xzf ${JRE_FILE} && \
    mv ${UNARCHIVE_DIR_NAME} ${JRE_DIR} && \
    rm -f ${JRE_FILE} && \
    mv ${JRE_DIR} ${JAVA_HOME}

# JAVA_HOME PATH 등록
ENV PATH="$PATH:$JAVA_HOME/bin"