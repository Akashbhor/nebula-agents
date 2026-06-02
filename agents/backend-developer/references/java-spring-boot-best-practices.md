# Java / Spring Boot Backend Best Practices

Guidance for Java backend implementations that use Spring Boot, Spring MVC or WebFlux, Spring Data, and common JVM tooling.

## Principles
- Keep business logic in service/domain layers, not controllers
- Use clear package boundaries and feature-local modules where practical
- Prefer constructor injection and explicit interfaces for cross-layer dependencies
- Validate request input close to the API boundary
- Map persistence models deliberately; do not leak JPA entities everywhere
- Keep transactions small and explicit

## Recommended Stack Patterns
- Spring Boot for application bootstrap and dependency wiring
- Spring Web MVC or WebFlux for HTTP APIs
- Spring Validation for request validation
- Spring Security for authN/authZ integration
- Spring Data JPA or JDBC depending on persistence needs
- Flyway or Liquibase for database migrations
- JUnit 5 + Mockito + Testcontainers for tests

## Checklists
- Controllers are thin and delegate to services
- DTOs are separated from persistence entities
- Validation errors are returned consistently
- Security rules are enforced at the service or endpoint boundary
- Database changes are versioned with migrations
- Integration tests cover repository and API behavior

## Notes
- Keep framework-specific code inside the product repo, not in `nebula-agents`.
- If the product uses a non-default folder layout such as `portal/` or `services/`, bind it in `BLUEPRINT.md` and `code-index.yaml` rather than assuming `engine/`.
