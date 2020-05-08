FROM mrbluecorp/openjdk:11.0.5-jdk

MAINTAINER secr3t <secr3t@mrblue.com>

ENV APM_AGENT_VER 1.15.0
ENV APM_AGENT_URL "https://search.maven.org/remotecontent?filepath=co/elastic/apm/elastic-apm-agent/$APM_AGENT_VER/elastic-apm-agent-$APM_AGENT_VER.jar"

RUN wget $APM_AGENT_URL -O apm-agent.jar