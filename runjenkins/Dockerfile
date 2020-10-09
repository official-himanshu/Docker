FROM openjdk:8


RUN mkdir -p ~/.jenkins
COPY jenkins.war .

EXPOSE 8080
CMD ["java","-jar","jenkins.war"]
