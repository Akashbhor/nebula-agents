---
template: test-plan
version: 2.0
applies_to: quality-engineer
---

# Test Plan — F####-{slug} run {run-id}

> File name in feature evidence package: `test-plan.md`. Required per §10/§14 for every completed terminal feature. QE-owned.

## Story-to-AC Mapping

For every story in scope, map each AC to the test(s) that will validate it.

| Story | AC | Lane | Test ID | Owner |
|-------|----|------|---------|-------|

## Test Strategy

- Unit tests (developer-owned) — lanes/frameworks/locations
- Component tests (developer-owned)
- Integration tests (QE-owned)
- E2E tests (QE-owned)
- API tests (QE-owned)
- Accessibility tests (QE-owned)

## Developer-vs-QE Test Ownership

Explicit assignment so reviewers know which lanes were the developer's responsibility vs QE's.

## Test Data / Fixtures

- Users / personas
- Seed data
- Mock fixtures vs real-DB integration

## Happy / Edge / Error / Auth / Accessibility / Regression Cases

Enumerate the case classes covered for this feature.

## Risks And Mitigations

Known risks, mitigation per risk, residual risk after mitigation.

## Recommendations (when `WITH RECOMMENDATIONS`)

§15 canonical bullet form. Severity `low`/`medium`/`high`/`critical`.

## Result

One of: `PASS`, `PASS WITH RECOMMENDATIONS`, `FAIL`.
