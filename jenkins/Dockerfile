# Tomcat 9 image

FROM anupverma/tomcat9:latest

WORKDIR /app/jenkins

# Download and Install Jenkins into Tomcat
ADD http://mirrors.jenkins.io/war-stable/latest/jenkins.war .
RUN mv jenkins.war $CATALINA_HOME/webapps

RUN pwd
RUN ls -al
RUN ls -al $CATALINA_HOME
RUN ls -al $CATALINA_HOME/webapps

RUN rm -f jenkins.war

# Add packages that may be needed for Jenkins
RUN apt-get update && apt-get install -y git groovy

# Start Tomcat
CMD ["catalina.sh", "run"]
