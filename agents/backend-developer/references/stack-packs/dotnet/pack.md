# .NET Backend Stack Pack

Use this pack for ASP.NET Core, Minimal APIs, Controllers, EF Core, and related .NET backend work.

## Stack Profile

- Framework: ASP.NET Core / Minimal APIs / Controllers
- ORM: EF Core
- Validation: JSON Schema / NJsonSchema where the product uses shared schemas
- Authorization: policy-based auth or Casbin-backed integration when required by the product
- Logging: structured logging with Serilog or the product-standard logger
- Testing: xUnit, Shouldly, Testcontainers

## Working Rules

- Keep business logic out of controllers and endpoints.
- Use DI consistently.
- Keep migrations explicit and versioned.
- Treat EF Core entities and API DTOs as separate models.
- Enforce audit, authorization, and validation on every mutation path.

## Expected References

- `agents/backend-developer/references/clean-architecture-guide.md`
- `agents/backend-developer/references/code-patterns.md`
- `agents/backend-developer/references/ef-core-patterns.md`

## Notes

- This pack holds the .NET-specific assumptions that used to sit in the base backend skill.
- Do not copy these assumptions into other backend stacks.
