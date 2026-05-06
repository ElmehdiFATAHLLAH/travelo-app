FROM eclipse-temurin:23-jdk AS build

WORKDIR /workspace

COPY .mvn .mvn
COPY mvnw pom.xml ./

RUN chmod +x mvnw && ./mvnw -B -ntp dependency:go-offline

COPY src src

RUN ./mvnw -B -ntp -DskipTests package


FROM eclipse-temurin:23-jdk AS runtime

WORKDIR /app

RUN useradd --uid 10001 --create-home appuser

RUN apt-get update && apt-get install -y curl

COPY --from=build /workspace/target/*.jar /app/app.jar

EXPOSE 8080

USER 10001

ENTRYPOINT ["java", "-XX:MaxRAMPercentage=75.0", "-jar", "/app/app.jar"]