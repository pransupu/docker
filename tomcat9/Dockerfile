# Tomcat 9 image

FROM anupverma/java8:latest

ENV TOMCAT_MAJOR=9
ENV TOMCAT_VER=9.0.0.M21

WORKDIR /app/tomcat$TOMCAT_MAJOR

# Install Tomcat
ADD http://mirrors.ibiblio.org/apache/tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VER/bin/apache-tomcat-$TOMCAT_VER.tar.gz .
RUN tar -xvzf apache-tomcat-$TOMCAT_VER.tar.gz
RUN rm -f apache-tomcat-$TOMCAT_VER.tar.gz

# Configure environment
ENV CATALINA_HOME=/app/tomcat$TOMCAT_MAJOR/apache-tomcat-$TOMCAT_VER
ENV PATH=$CATALINA_HOME/bin:$PATH

# Start Tomcat
CMD ["catalina.sh", "run"]
