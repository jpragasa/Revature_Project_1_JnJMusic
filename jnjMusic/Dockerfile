# start with the alpine linux tomcat image
FROM tomcat:8.5-jdk8-openjdk

# switch to the CATALINA_HOME directory
WORKDIR $CATALINA_HOME

ENV url=jdbc:postgresql://database-1.cis8fsnxixal.us-east-1.rds.amazonaws.com:5432/myDatabase
ENV name=jean
ENV password=P@ssword

# create a reference to some file on the physical machine (optional)
ARG WAR_FILE=./target/*.war

# copy the file from the physical machine to the webapps dir in the PWD
COPY $WAR_FILE ./webapps

# EXPOSE port 8080
EXPOSE 8080

# execute this command to start tomcat
CMD ["catalina.sh", "run"]



# image creation complete
