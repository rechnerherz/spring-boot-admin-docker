FROM java:8-jre-alpine

EXPOSE 8080

### Add microservice artifact
COPY spring-boot-admin-docker-2.0.1.jar /opt/spring-boot-admin-docker-2.0.1.jar

WORKDIR /opt
ENTRYPOINT ["java", "-jar", "spring-boot-admin-docker-2.0.1.jar"]