FROM centos:7.6.1810

MAINTAINER wyparks2 <wyparks2@mrblue.com>

# Install Packages
RUN yum update -y && \
    yum install -y wget && \
    yum clean all

# 언어 설정
RUN localedef -f UTF-8 -i ko_KR ko_KR.UTF-8
ENV LC_ALL ko_KR.UTF-8
ENV LANGUAGE ko_KR.UTF-8

# 타임존 설정
ENV TZ=Asia/Seoul
RUN ln -snf /usr/share/zoneinfo/${TZ} /etc/localtime && \
    echo ${TZ} > /etc/timezone
