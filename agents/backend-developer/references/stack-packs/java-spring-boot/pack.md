# Java / Spring Boot Backend Stack Pack

Use this pack for Spring Boot backend work, including Spring MVC or WebFlux, Spring Data, and JVM tooling.

## Stack Profile

- Framework: Spring Boot
- HTTP: Spring MVC or WebFlux
- Validation: Spring Validation / Bean Validation / Hibernate Validator
- Authorization: Spring Security or the product-standard auth mechanism
- Persistence: Spring Data JPA or JDBC
- Migrations: Flyway or Liquibase
- Testing: JUnit 5, Mockito, Testcontainers
- Logging: SLF4J / Logback or the product-standard logger

## Working Rules

- Keep controllers thin.
- Keep business logic in service/domain layers.
- Use constructor injection.
- Keep DTOs separate from persistence entities.
- Make transactions explicit.
- Return errors and validation failures consistently.

## Expected References

- `agents/backend-developer/references/clean-architecture-guide.md`
- `agents/backend-developer/references/code-patterns.md`

## Notes

- This pack holds the Java-specific assumptions that should not live in the base backend skill.
- Do not mix these assumptions into the .NET pack or the generic backend role.
