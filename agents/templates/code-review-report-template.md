# Code Review Report — F####-{slug} run {run-id}

> Required per §10 for every completed terminal feature. Code Reviewer-owned.

## Reviewed Files

List the source/test paths reviewed in this pass. Cite `scm.diff_artifact` for the canonical changed-file set.

## Validation Artifacts

Test results, coverage, static-analysis outputs, lint logs that the reviewer relied on.

## Severity-Ranked Findings

Use the §15 severity scale (`low`/`medium`/`high`/`critical`). Findings that are blocking become `REQUEST CHANGES` or `REJECTED`. Findings deferred as recommendations follow the §15 canonical bullet.

```text
- [high] <finding text> — owner: <name-or-role>; follow-up: <ticket-id-or-deferred-no-followup>
```

`high`/`critical` recommendations require explicit PM mitigation in `pm-closeout.md` Recommendation Acceptances using the §15 PM Acceptance Line Format with `mitigation:` prefix.

## Non-Blocking Recommendations With Owner/Follow-up

`low`/`medium` recommendations live here, each with the canonical bullet.

## Vertical-Slice Completeness

Confirm the change has end-to-end coverage (data → API → UI → tests). Note any seams left undone.

## AC / Test Adequacy

Confirm tests reflect AC. Surface any AC-without-test or test-without-AC pairs.

## Architecture Compliance

Cross-check against assembly plan and boundary policy. Note any new dependencies, layer violations, or pattern deviations.

## Coverage Verification

Verify `coverage-report.md` numbers match the raw coverage artifact. Flag drift.

## Result

One of: `APPROVED`, `APPROVED WITH RECOMMENDATIONS`, `REQUEST CHANGES`, `REJECTED`.
