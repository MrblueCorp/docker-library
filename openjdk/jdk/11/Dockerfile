FROM mrbluecorp/centos:7

MAINTAINER wyparks2 <wyparks2@mrblue.com>

ENV JDK_VERSION 11.0.2
ENV JDK_DIR jdk-${JDK_VERSION}
ENV JDK_FILE jdk-${JDK_VERSION}.tar.gz
ENV JAVA_HOME /usr/local/${JDK_DIR}

ENV DOWNLOAD_URL https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.2%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.2_9.tar.gz
ENV UNARCHIVE_DIR_NAME jdk-11.0.2+9

# JDK 설치
RUN cd /usr/local/src && \
    wget ${DOWNLOAD_URL} -O ${JDK_FILE} && \
    tar xzf ${JDK_FILE} && \
    mv ${UNARCHIVE_DIR_NAME} ${JDK_DIR} && \
    rm -f ${JDK_FILE} && \
    mv ${JDK_DIR} ${JAVA_HOME}

# JAVA_HOME PATH 등록
ENV PATH="$PATH:$JAVA_HOME/bin"
