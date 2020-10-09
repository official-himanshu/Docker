
# Build stage

FROM maven AS build
COPY src /usr/src/app/src
COPY pom.xml /usr/src/app
RUN mvn -f /usr/src/app/pom.xml clean package

FROM openjdk
COPY --from=build /usr/src/app/target/my-app-1.0-SNAPSHOT.jar /usr/app/my-app-1.0-SNAPSHOT.jar
ENTRYPOINT ["java","-jar","/usr/app/my-app-1.0-SNAPSHOT.jar"]


