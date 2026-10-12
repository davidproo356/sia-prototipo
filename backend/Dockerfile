# Plantilla de imagen backend. NO compilará hasta existir una aplicación Java.
# En Compose el contexto de construcción es la raíz.
FROM maven:3.9.11-eclipse-temurin-21 AS build
WORKDIR /workspace
COPY backend/pom.xml backend/pom.xml
RUN cd backend && mvn -B -ntp dependency:go-offline
COPY backend/src backend/src
RUN cd backend && mvn -B -ntp package -DskipTests

FROM eclipse-temurin:21-jre
WORKDIR /app
RUN groupadd --system sia && useradd --system --gid sia --home-dir /app sia
COPY --from=build /workspace/backend/target/*.jar /app/app.jar
USER sia
EXPOSE 8080
ENTRYPOINT ["java", "-jar", "/app/app.jar"]
