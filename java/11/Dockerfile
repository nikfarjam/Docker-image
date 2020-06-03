# escape=`
FROM opensuse/leap:latest

RUN mkdir /tmp/java && cd $_ && `
    zypper refresh && `
    zypper --non-interactive install tar gzip curl && `
    curl https://download.java.net/java/GA/jdk11/9/GPL/openjdk-11.0.2_linux-x64_bin.tar.gz `
    | tar xz && `
    cd jdk-11.0.2 && `
    ./bin/jlink --module-path ./jmods/ --compress=2 `
    --add-modules java.base,java.sql,java.desktop,java.management,java.naming,java.logging,java.security.jgss,java.instrument,java.xml,jdk.unsupported `
    --no-header-files --no-man-pages --output /opt/java && `
    mkdir -p /usr/app && `
    cd $_ && rm -Rf /tmp/*

ENV JAVA_HOME=/opt/java
ENV PATH="$PATH:$JAVA_HOME/bin"

CMD ["bash"]