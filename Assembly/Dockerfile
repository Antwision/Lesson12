FROM ubuntu:22.04
RUN apt update && apt install \
    git \
    maven -y \
    &&  rm -rf /var/lib/apt/lists/*
WORKDIR /usr/src/app/
RUN git clone https://github.com/shephertz/App42PaaS-Java-MySQL-Sample.git
WORKDIR /usr/src/app/App42PaaS-Java-MySQL-Sampl/
COPY Config.properties ./WebContent/
RUN mvn package
