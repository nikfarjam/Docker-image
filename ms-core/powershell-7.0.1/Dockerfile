# escape = `
FROM debian:buster-slim

ARG POWERSHELL_URL=https://github.com/PowerShell/PowerShell/releases/download/v7.0.1/powershell-7.0.1-linux-x64.tar.gz
ENV POWERSHELL_HOME=/opt/microsoft/powershell/7
WORKDIR /usr/app

RUN apt-get update &&`
    apt-get install -y curl &&`
    rm -rf /var/lib/apt/lists/* &&`
    mkdir -p ${POWERSHELL_HOME} &&`
    cd $_

ADD ${POWERSHELL_URL} .

ENV PATH=${JAVA_HOME}/bin:$PATH

CMD ["pwsh"]