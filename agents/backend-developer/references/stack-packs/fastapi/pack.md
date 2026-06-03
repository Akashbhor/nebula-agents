# Python / FastAPI Backend Stack Pack

Use this pack for FastAPI-based backend work, including Python API services, async HTTP handlers, and lightweight service layers.

## Stack Profile

- Framework: FastAPI
- API Style: async HTTP endpoints or routers
- Validation: Pydantic models / product-standard schema validation
- Authorization: product-standard authN/authZ mechanism
- Persistence: SQLAlchemy, SQLModel, or direct DB access depending on the product
- Migrations: Alembic or the product-standard migration tool
- Testing: pytest, httpx, Testcontainers where applicable
- Logging: structured Python logging or the product-standard logger

## Working Rules

- Keep route handlers thin.
- Keep business logic in service/domain modules.
- Keep request/response models separate from persistence models.
- Make async boundaries explicit.
- Keep migrations versioned and reversible.
- Enforce validation, authorization, and audit behavior consistently.

## Expected References

- `agents/backend-developer/references/clean-architecture-guide.md`
- `agents/backend-developer/references/code-patterns.md`

## Notes

- This pack holds the Python/FastAPI-specific assumptions that should not live in the base backend skill.
- Do not mix these assumptions into the .NET or Java packs.
