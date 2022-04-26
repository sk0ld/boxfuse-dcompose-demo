Test usage of docker compose with maven & tomcat

Tested on Ubuntu 20.04

apt update && apt install -y git docker.io

To install docker compose: follow https://docs.docker.com/compose/install/ or https://docs.docker.com.zh.xy2401.com/v17.12/compose/install/#install-compose

Cloning repository & preparing docker image:

git clone https://github.com/sk0ld/boxfuse-dcompose-demo.git

cd boxfuse-dcompose-demo/

docker-compose up -d

To check boxfuse app is working on tomcat:
http://your_ip_or_hostname:8080/hello-1.0

To stop docker container:

docker-compose stop
