FROM mrbluecorp/openjdk:11.0.5-jre

MAINTAINER secr3t <secr3t@mrblue.com>

ENV MVN_VERSION 3.6.3
ENV MVN_DIR apache-maven-${MVN_VERSION}
ENV MVN_TAR ${MVN_DIR}.tar.gz
ENV MVN_DOWNLOAD_URL http://apache.tt.co.kr/maven/maven-3/${MVN_VERSION}/binaries/apache-maven-${MVN_VERSION}-bin.tar.gz
ENV MVN_HOME /usr/local/maven

RUN cd /usr/local/src && \
    wget ${MVN_DOWNLOAD_URL} -O ${MVN_TAR} && \
    tar -xvzf ${MVN_TAR} && \
    mv ${MVN_DIR} ${MVN_HOME} && \
    rm -f ${MVN_TAR} && \
    ln -s ${MVN_HOME}/bin/mvn /usr/bin/mvn 

ENV PATH="$PATH:$MVN_HOME/bin"