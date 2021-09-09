FROM maven:3.6.3-jdk-8 AS build-env
WORKDIR /app

COPY pom.xml ./

COPY . ./


FROM openjdk:8-jre-alpine
EXPOSE 9003
WORKDIR /app

COPY ./target/spring-boot-cassandra-0.0.1-SNAPSHOT.jar ./
CMD ["java", "-jar", "spring-boot-cassandra-0.0.1-SNAPSHOT.jar"]