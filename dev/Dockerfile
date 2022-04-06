FROM ubuntu:20.04
ENV TZ=Europe/Moscow
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone 
ENV BFAPP=boxfuse-sample-java-war-hello
RUN DEBIAN_FRONTEND=noninteractive apt-get update && apt-get install -y git maven
RUN git clone https://github.com/boxfuse/$BFAPP.git
WORKDIR /$BFAPP
RUN mvn package -DskipTests && cp target/*.war /usr/local/src
CMD ["mvn"]