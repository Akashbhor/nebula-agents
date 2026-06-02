# Java / Spring Boot Containerization Guide

Use this alongside `containerization-guide.md` when the backend is Java-based.

## Backend Detection Signals
- `pom.xml` or `build.gradle`
- `src/main/java/`
- `src/main/resources/application.properties` or `application.yml`
- `@SpringBootApplication`
- Maven Wrapper (`mvnw`) or Gradle Wrapper (`gradlew`)

## Runtime Extraction
- Java version: `maven.compiler.source` / `maven.compiler.target` or toolchain config
- App port: `server.port` or `application.properties` / `application.yml`
- Database: `spring.datasource.*`
- Auth: `Spring Security`, OIDC, JWT, or custom filter chain
- Health endpoints: `actuator/health` when Spring Boot Actuator is enabled

## Dockerfile Pattern
- Use a multi-stage build
- Builder stage: Maven or Gradle with JDK
- Runtime stage: JRE or slim JDK image
- Copy the built JAR only into the runtime stage
- Run as a non-root user
- Expose the detected app port

## Example Build Flow
```bash
./mvnw test
./mvnw package -DskipTests
```

## Compose Notes
- Add a database service if the app depends on MySQL/PostgreSQL
- Wire `SPRING_DATASOURCE_URL`, `SPRING_DATASOURCE_USERNAME`, and `SPRING_DATASOURCE_PASSWORD`
- Add healthchecks that wait on the Actuator health endpoint when available
- Keep frontend and backend as separate services when the UI is a `portal/` or SPA

## What Not to Do
- Do not bake secrets into the image
- Do not rely on `latest` tags for runtime images
- Do not assume the product uses `engine/` if the blueprint declares another backend folder
