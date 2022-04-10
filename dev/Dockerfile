FROM ubuntu:20.04
ENV TZ=Europe/Moscow
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
ENV BFAPP=boxfuse-sample-java-war-hello
RUN DEBIAN_FRONTEND=noninteractive apt-get update && apt-get install -y git maven
WORKDIR /usr/share/src-data
RUN git clone https://github.com/boxfuse/$BFAPP.git ./
RUN mvn package -DskipTest

