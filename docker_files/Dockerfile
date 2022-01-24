FROM ubuntu:focal
COPY resources  /

RUN apt update \
&& DEBIAN_FRONTEND='noninteractive' apt install git -yq \
&& DEBIAN_FRONTEND='noninteractive' apt install vim -yq \
&& DEBIAN_FRONTEND='noninteractive' apt install default-jre -yq \
&& DEBIAN_FRONTEND='noninteractive' apt install openjdk-11-jre-headless -yq \
&& DEBIAN_FRONTEND='noninteractive' apt install openjdk-8-jre-headless -yq \
&& DEBIAN_FRONTEND='noninteractive' apt install default-jdk -yq

RUN git clone https://github.com/spring-petclinic/spring-framework-petclinic.git \
&& sed -i 's/Welcome/Mor_was_here/g' /spring-framework-petclinic/src/main/resources/messages/messages.properties
WORKDIR /spring-framework-petclinic
ENTRYPOINT ["./mvnw","jetty:run-war"] 


