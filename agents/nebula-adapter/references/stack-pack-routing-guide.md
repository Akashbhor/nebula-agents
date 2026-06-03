# Stack Pack Routing Guide

This guide defines how Nebula resolves the active stack pack for a product session.

## Purpose

Select the product's declared backend and frontend stack families once per session, then load only the references needed by the active role.

Do not merge stack-specific content into the base agent skills.

## Selection Order

1. Read `{PRODUCT_ROOT}/planning-mds/BLUEPRINT.md`
2. Read `{PRODUCT_ROOT}/planning-mds/knowledge-graph/code-index.yaml`
3. Resolve the declared backend and frontend stack families and stack packs
4. Load the matching stack-pack references under `agents/**/references/`
5. Keep the loaded pack scoped to the current session or task

## Layout Rules

- Treat the declared backend and frontend stack families as first-class when they are documented in the product blueprint.
- Do not assume `.NET`, `Java/Spring Boot`, `Python/FastAPI`, `React`, `Streamlit`, or `htmx` unless the product explicitly uses that stack.
- If the stack pack depends on a specific runtime or build tool, prefer that pack's reference files over the generic base skill.

## Pack Separation

- `backend-developer` remains role-based
- `frontend-developer` remains role-based
- `devops` remains deployment-oriented
- `nebula-adapter` resolves and documents the active pack

## Validation

- Confirm the active stack packs match the product blueprint
- Confirm router entries point to the relevant stack references
- Confirm the base role files do not accumulate stack-specific assumptions
