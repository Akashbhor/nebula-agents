# Test Execution Report — F####-{slug} run {run-id}

> Required per §10. Quality Engineer-owned. The QE verdict artifact for `role_results['Quality Engineer']`.

## Commands Executed

```text
- pnpm test --runInBand → 0 failures
- dotnet test → 0 failures
- pnpm exec playwright test → 2 retries, 0 failures
```

Each line should appear in `commands.log` with matching exit codes.

## Pass/Fail Counts

| Lane | Total | Pass | Fail | Skip | Retries |
|------|------:|-----:|-----:|-----:|--------:|
| Unit (engine) | 142 | 142 | 0 | 0 | 0 |
| Unit (experience) | 87 | 87 | 0 | 0 | 0 |
| Component | 24 | 24 | 0 | 0 | 0 |
| Integration | 18 | 18 | 0 | 0 | 0 |
| E2E | 6 | 6 | 0 | 0 | 2 |

## Skipped Tests And Rationale

List skipped tests by ID and why. An empty section may say `- None`.

## Raw Test Artifact Paths

Cite the path of every test artifact relied upon (junit XML, playwright reports). Validator checks they resolve.

- `artifacts/test-results/junit-engine.xml`
- `artifacts/test-results/playwright-report/`

## Failed / Retried Command History

Document the chronology of any failure-then-retry events. Helps reviewers reason about flakiness vs real defects.

## AC Coverage Result

Map each AC to its evidence and final outcome (covered / partial / deferred).

## Recommendations (when `WITH RECOMMENDATIONS`)

Use §15 canonical bullet. Severity `low`/`medium`/`high`/`critical`.

## Result

One of: `PASS`, `PASS WITH RECOMMENDATIONS`, `FAIL`.
