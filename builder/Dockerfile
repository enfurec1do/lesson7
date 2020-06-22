
FROM ubuntu:18.04

# Tomcat Version
ENV TOMCAT_VERSION_MAJOR 8
ENV TOMCAT_VERSION_FULL  8.5.42

RUN apt update && apt install -y \
    maven \
    git \
    default-jdk

WORKDIR git

RUN git clone https://github.com/ewolff/user-registration-V2.git && cd user-registration-V2 && ./mvnw -pl user-registration-application -am install

RUN cp ./user-registration-V2/user-registration-application/target/user-registration-application-0.0.1-SNAPSHOT.war /build
