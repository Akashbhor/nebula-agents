# Adapting to Different Tech Stacks

This framework is reusable across stacks. The agent roles and templates stay the same; only stack-specific references and examples need adjustments.

## Quick Checklist

1) Identify the target stack (backend, frontend, database, infra/auth).
2) Replace or add stack-specific reference guides under `agents/**/references/`.
3) Update `agents/README.md` tech stack assumptions to match your stack.
4) Update any scripts that are stack-specific (test runners, scaffolds).
5) Keep existing templates unchanged; add new stack-specific or compatibility SKILL.md files only when introducing a new role or a small stack pack.
6) Use the `nebula-adapter` role when the change is about framework routing, stack packs, or non-default product layouts.

## What Works Unchanged (Any Tech Stack)

- All existing agent `SKILL.md` files, plus any explicitly added compatibility roles
- All templates in `agents/templates/`
- Product Manager, Architect, QA, Security, Code Reviewer roles
- Generic references (clean architecture, testing best practices, UX, accessibility, etc.)

## What Needs Updating

### Example: FastAPI Backend

Replace or add:
- `agents/backend-developer/references/dotnet-best-practices.md` → `fastapi-best-practices.md`
- `agents/backend-developer/references/ef-core-patterns.md` → `sqlalchemy-patterns.md`

Keep unchanged:
- `clean-architecture-guide.md` (generic)
- `SKILL.md` (generic responsibilities)

### Example: Java / Spring Boot Backend

Replace or add:
- `agents/backend-developer/references/dotnet-best-practices.md` → `java-spring-boot-best-practices.md`
- `agents/devops/references/containerization-guide.md` → add Java/Spring Boot detection and Dockerfile patterns

Keep unchanged:
- `clean-architecture-guide.md` (generic)
- `SKILL.md` (generic responsibilities)

### When to Use Nebula Adapter

Use the `nebula-adapter` role when the change is not product code but framework wiring:
- adding or routing a new stack-specific guide
- supporting a non-default product layout such as `portal/`, `api/`, or `services/`
- updating framework docs so the stack/layout assumptions stay consistent

### Example: Vue.js Frontend

Replace or add:
- `agents/frontend-developer/references/react-best-practices.md` → `vue-best-practices.md`
- Update component examples in `testing-guide.md` if they are React-specific

Keep unchanged:
- `typescript-patterns.md`
- `accessibility-guide.md`
- `ux-principles.md`

## Guidance

- Prefer adding new stack-specific reference files over renaming existing ones to avoid breaking links.
- If you need a new stack, add a small “stack pack” under each role’s `references/` folder.
- If the product uses a different frontend root name such as `portal/`, declare that in `{PRODUCT_ROOT}/planning-mds/BLUEPRINT.md` and bind it in `code-index.yaml` rather than hardcoding `experience/` in framework docs.
- Keep solution-specific examples in `{PRODUCT_ROOT}/planning-mds/`, never in `agents/`.
