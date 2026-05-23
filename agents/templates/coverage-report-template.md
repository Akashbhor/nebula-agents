# Coverage Report — F####-{slug} run {run-id}

> Required per §10 — the file must exist even when coverage is waived. QE-owned.

## Coverage Target And Actual Per Layer

| Layer | Target | Actual | Source |
|-------|------:|------:|--------|
| Unit (engine) | 80% | 86% | `artifacts/coverage/engine-cobertura.xml` |
| Unit (experience) | 70% | 78% | `artifacts/coverage/experience-lcov.info` |
| Integration | 60% | 64% | `artifacts/coverage/integration-cobertura.xml` |

## Raw Artifact Paths

Cite each coverage artifact path. External (implementation-layer) coverage paths are allowed and should be linked from `artifact-trace.md`.

## Feature-Scoped Notes

Coverage scoped to this feature's changed surfaces. Note any cross-feature regressions or trade-offs.

## Waiver Block (when coverage cannot be produced or is below target)

Required only when `manifest.waivers.coverage` is set. The waiver block here must echo the waiver fields and the PM Acceptance Line in `pm-closeout.md`.

- Owner: <Quality Engineer name>
- Date: YYYY-MM-DD
- Scope: <what is waived>
- Reason: <why coverage cannot be produced or is below target>
- Follow-up: <ticket or "None">

PM Acceptance must use `<identifier> = coverage` per §15 PM Acceptance Line Format.

## Recommendations (when `WITH RECOMMENDATIONS`)

§15 canonical bullet form. Severity `low`/`medium`/`high`/`critical`.

## Result

One of: `PASS`, `PASS WITH RECOMMENDATIONS`, `FAIL`.
