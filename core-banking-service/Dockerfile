FROM eclipse-temurin:21.0.2_13-jre-alpine

LABEL maintainer="rlakshmana50@gmail.com"

WORKDIR /app

VOLUME /main-app

COPY build/libs/core-banking-service-0.0.1-SNAPSHOT.jar app.jar
COPY wait-for-it.sh wait-for-it.sh

RUN chmod +x wait-for-it.sh && apk add --no-cache bash

EXPOSE 8092

ENTRYPOINT ["java", "-Dspring.profiles.active=docker", "-jar", "app.jar"]
