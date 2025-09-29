# Use Tomcat 9 with a recent JDK
FROM tomcat:9.0-jdk17

# Remove default ROOT app
RUN rm -rf /usr/local/tomcat/webapps/ROOT

# Copy the built WAR into the image as ROOT.war so app serves from "/"
# Ensure your build produces target/hello-servlet.war
COPY target/hello-servlet.war /usr/local/tomcat/webapps/ROOT.war

EXPOSE 8080

CMD ["catalina.sh", "run"]
