FROM alpine:3.10.3

ADD . /workspace

WORKDIR /workspace

RUN apk update &&\
    apk add openjdk8 gcc libc-dev cargo wget

RUN wget -qO - "https://github.com/sbt/sbt/releases/download/v$sbt_version/sbt-$sbt_version.tgz" >/tmp/sbt.tgz
RUN tar xzf /tmp/sbt.tgz -C 

ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk
ENV PATH="$JAVA_HOME/bin:${PATH}"
