FROM ubuntu:20.04 
ENV BFAPP=boxfuse-sample-java-war-hello
RUN DEBIAN_FRONTEND=noninteractive apt-get update && apt-get install -y git maven
RUN git clone https://github.com/boxfuse/$BFAPP.git
WORKDIR /$BFAPP
RUN mvn package -DskipTests
CMD ["mvn"]