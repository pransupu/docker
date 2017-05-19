# Oracle JDK Image docker

# Start with Ubuntu as the base OS image
FROM ubuntu:16.04

# Install and configure Oracle java from local downloaded image
WORKDIR /app/java
ADD http://mrepescoeapp5.phx.lab.aexp.com/files/jdk-8u131-linux-x64.tar.gz .
RUN tar -xvzf jdk-8u131-linux-x64.tar.gz
RUN rm -f jdk-8u131-linux-x64.tar.gz
ENV PATH=/app/java/jdk1.8.0_131/bin:$PATH
ENV JAVA_HOME=/app/java/jdk1.8.0_131

CMD ["java", "-version"]

