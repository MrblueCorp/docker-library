FROM mrbluecorp/centos:7

MAINTAINER wyparks2 <wyparks2@mrblue.com>

# Install node
ENV NODE_VERSION 10.15.3
RUN curl -sL https://rpm.nodesource.com/setup_10.x | bash - && \
    yum install -y nodejs-$NODE_VERSION

# Install yarn
ENV YARN_VERSION 1.13.0
RUN npm install --global yarn@$YARN_VERSION