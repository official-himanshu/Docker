FROM maven:3.6.3-openjdk-8
COPY src /usr/src/hellodocker/src
COPY pom.xml /usr/src/hellodocker
RUN mvn -f /usr/src/hellodocker/pom.xml clean package

FROM openjdk:8
WORKDIR /app/
COPY --from=0 /usr/src/hellodocker/target/hellodocker-1.0-SNAPSHOT.jar .
RUN java -jar hellodocker-1.0-SNAPSHOT.jar
ENTRYPOINT ["java","-jar","hellodocker-1.0-SNAPSHOT.jar"]
#CMD ["java","-jar","hellodocker-1.0-SNAPSHOT.jar"]
