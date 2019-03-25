FROM mrbluecorp/centos:7

MAINTAINER wyparks2 <wyparks2@mrblue.com>

ENV JRE_VERSION 11.0.2
ENV JRE_DIR jre-${JRE_VERSION}
ENV JRE_FILE jre-${JRE_VERSION}.tar.gz
ENV JAVA_HOME /usr/local/${JRE_DIR}

ENV DOWNLOAD_URL https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.2%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.2_9.tar.gz
ENV UNARCHIVE_DIR_NAME jdk-11.0.2+9-jre

# JRE 설치
RUN cd /usr/local/src && \
    wget ${DOWNLOAD_URL} -O ${JRE_FILE} && \
    tar xzf ${JRE_FILE} && \
    mv ${UNARCHIVE_DIR_NAME} ${JRE_DIR} && \
    rm -f ${JRE_FILE} && \
    mv ${JRE_DIR} ${JAVA_HOME}

# JAVA_HOME PATH 등록
ENV PATH="$PATH:$JAVA_HOME/bin"
