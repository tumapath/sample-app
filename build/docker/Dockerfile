FROM java:8

MAINTAINER Selva Umapathy <tamizhselvanu@gmail.com>

ARG RELEASE=dropwizard-example-1.0-release

RUN mkdir /data
ENV RELEASE ${RELEASE} 

## Download the appropriate jar version from the maven repo	
## mvn org.apache.maven.plugins:maven-dependency-plugin:2.1:get \
##    -DrepoUrl=http://nexus.org.com \
##   -Dartifact=sample-app:sample-app:$release

## For this example copying the snapshot from local repo
ADD target/${RELEASE}.jar /data/app.jar

ADD example.yml /data/example.yml

WORKDIR /data

EXPOSE 9000

CMD java -jar app.jar server example.yml






