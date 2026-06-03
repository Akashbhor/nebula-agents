# Adapting to Different Tech Stacks

This framework is reusable across stacks. The agent roles and templates stay the same; only stack-specific references and examples need adjustments.

## Quick Checklist

1) Identify the target stack (backend, frontend, database, infra/auth).
2) Replace or add stack-specific reference guides under `agents/**/references/`.
3) Update `agents/README.md` tech stack assumptions to match your stack.
4) Update any scripts that are stack-specific (test runners, scaffolds).
5) Keep existing templates unchanged; add new stack-specific or compatibility SKILL.md files only when introducing a new role or a small stack pack.
6) Use the `nebula-adapter` role when the change is about framework routing or stack packs.

## What Works Unchanged (Any Tech Stack)

- All existing agent `SKILL.md` files, plus any explicitly added compatibility roles
- All templates in `agents/templates/`
- Product Manager, Architect, QA, Security, Code Reviewer roles
- Generic references (clean architecture, testing best practices, UX, accessibility, etc.)

## What Needs Updating

### Example: FastAPI Backend

Replace or add:
- `agents/backend-developer/references/stack-packs/dotnet/pack.md` → `stack-packs/fastapi/pack.md`

Keep unchanged:
- `clean-architecture-guide.md` (generic)
- `SKILL.md` (generic responsibilities)

### Example: Java / Spring Boot Backend

Replace or add:
- `agents/backend-developer/references/stack-packs/dotnet/pack.md` → `stack-packs/java-spring-boot/pack.md`
- `agents/devops/references/containerization-guide.md` → add Java/Spring Boot detection and Dockerfile patterns

Keep unchanged:
- `clean-architecture-guide.md` (generic)
- `SKILL.md` (generic responsibilities)

### Example: Frontend Stack Packs

Replace or add:
- `agents/frontend-developer/references/stack-packs/react/pack.md` → `stack-packs/streamlit/pack.md`
- `agents/frontend-developer/references/stack-packs/react/pack.md` → `stack-packs/htmx/pack.md`

Keep unchanged:
- `ux-audit-ruleset.md` (generic)
- `code-patterns.md` (shared implementation patterns)

### When to Use Nebula Adapter

Use the `nebula-adapter` role when the change is not product code but framework wiring:
- adding or routing a new stack-specific guide
- updating framework docs so the stack assumptions stay consistent

## Guidance

- Prefer adding new stack-specific reference files over renaming existing ones to avoid breaking links.
- If you need a new stack, add a small “stack pack” under each role’s `references/` folder.
- Keep solution-specific examples in `{PRODUCT_ROOT}/planning-mds/`, never in `agents/`.
