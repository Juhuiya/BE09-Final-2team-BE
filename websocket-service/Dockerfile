FROM openjdk:17-jdk-slim

WORKDIR /app

COPY gradlew .
COPY gradlew.bat .
COPY build.gradle .
COPY settings.gradle .
COPY gradle gradle
COPY src src

RUN chmod +x ./gradlew
RUN ./gradlew bootJar
RUN cp build/libs/*.jar app.jar

EXPOSE 8085

ENTRYPOINT ["java", "-jar", "app.jar"]