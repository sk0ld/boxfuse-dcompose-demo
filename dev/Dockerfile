FROM maven:3.5.2-jdk-8-alpine
RUN apk update
RUN apk add git
WORKDIR /usr/share/app-src
RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git ./
RUN mvn package -DskipTest