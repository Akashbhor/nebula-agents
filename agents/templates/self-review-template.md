# Self Review — F####-{slug} run {run-id}

> File name: `g2-self-review.md`. Required at G2 for every completed terminal feature per §10/§14.

## Scope Review

Confirm the implemented scope matches the assembly plan and PRD. Note any drift and how it was resolved.

## Acceptance Criteria Review

For each AC, name the test (or evidence) that validates it. Reference paths under the run folder.

- AC-1: covered by `test-execution-report.md` (unit lane)
- AC-2: covered by `artifacts/screenshots/feature-flow.png`

## Implementation Risks

Risks the implementer surfaces for the reviewer (refactor scope, data shape change, performance hotspot). Each risk includes a mitigation or a deferred follow-up.

## Validation Evidence

References to the validation artifacts produced or consulted: test results, coverage reports, scan outputs, KG / template validator runs.

## Recommendations (when `WITH RECOMMENDATIONS`)

Use the §15 canonical bullet:

```text
- [severity] <recommendation text> — owner: <name-or-role>; follow-up: <ticket-id-or-deferred-no-followup>
```

`high`/`critical` recommendations require PM mitigation in `pm-closeout.md` per §15 PM Acceptance Line Format.

## Result

One of: `PASS`, `PASS WITH RECOMMENDATIONS`, `FAIL`.
