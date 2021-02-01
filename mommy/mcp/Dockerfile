FROM mrbluecorp/openjdk:11.0.5-jdk

# ImageMagick 설치
ARG CACHEBUST=0
RUN yum upgrade -y
RUN yum install -y gcc php-devel php-pear && \
    yum install -y ImageMagick ImageMagick-devel
ARG CACHEBUST=1

# 언어 설정
# yum 패키지 설치 후 Locale이 변경될 수 있기 때문에 재설정한다. (yum 설치를 할 경우에만 설정)
RUN localedef -f UTF-8 -i ko_KR ko_KR.UTF-8
ENV LC_ALL ko_KR.UTF-8
ENV LANGUAGE ko_KR.UTF-8
