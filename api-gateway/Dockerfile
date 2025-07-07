FROM eclipse-temurin:17-jdk
WORKDIR /app

# Copia el JAR ya compilado (que incluye application.properties y application-docker.properties)
COPY target/*.jar app.jar

EXPOSE 8080

# Arranca con el perfil "docker" para que Spring cargue application-docker.properties
ENTRYPOINT ["java","-jar","app.jar","--spring.profiles.active=docker"]
