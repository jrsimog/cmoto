# Versión corregida (tag verificado en Docker Hub)
FROM maven:3.9.4-eclipse-temurin-21-alpine AS build  
WORKDIR /app
COPY pom.xml .
COPY src ./src
RUN mvn clean package -DskipTests

# Etapa de ejecución (se mantiene igual)
FROM eclipse-temurin:21-jdk-alpine
WORKDIR /app
COPY --from=build /app/target/*.jar app.jar
EXPOSE 8080
ENTRYPOINT ["java", "-jar", "app.jar"]

