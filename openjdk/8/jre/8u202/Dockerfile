FROM mrbluecorp/centos:7

MAINTAINER wyparks2 <wyparks2@mrblue.com>

ENV JAVA_VERSION 8u202
ENV JAVA_DIR jre-${JAVA_VERSION}
ENV JAVA_FILE jre-${JAVA_VERSION}.tar.gz
ENV JAVA_HOME /usr/local/${JAVA_DIR}

ENV DOWNLOAD_URL https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u202-b08/OpenJDK8U-jre_x64_linux_hotspot_8u202b08.tar.gz
ENV UNARCHIVE_DIR_NAME jdk8u202-b08-jre

# JAVA 설치
RUN cd /usr/local/src && \
    wget ${DOWNLOAD_URL} -O ${JAVA_FILE} && \
    tar xzf ${JAVA_FILE} && \
    mv ${UNARCHIVE_DIR_NAME} ${JAVA_DIR} && \
    rm -f ${JAVA_FILE} && \
    mv ${JAVA_DIR} ${JAVA_HOME}

# JAVA_HOME PATH 등록
ENV PATH="$PATH:$JAVA_HOME/bin"