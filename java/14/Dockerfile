# escape = `
FROM debian:buster-slim

ENV JAVA_URL=https://download.java.net/java/GA/jdk14.0.1/664493ef4a6946b186ff29eb326336a2/7/GPL/openjdk-14.0.1_linux-x64_bin.tar.gz
ENV JAVA_HOME=/usr/java/jdk-14.0.1
ENV PATH=${JAVA_HOME}/bin:$PATH
WORKDIR /usr/app

RUN apt-get update &&`
    apt-get install -y curl &&`
    rm -rf /var/lib/apt/lists/* &&`
    mkdir -p /usr/java &&`
    cd /usr/java &&`
    curl ${JAVA_URL} | tar xz

CMD ["jshell"]