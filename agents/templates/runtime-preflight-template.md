# Runtime Preflight — F####-{slug} run {run-id}

> File name: `g1-runtime-preflight.md`. Required at G1 when `runtime_bearing = true` per §10.

## Feature

- Feature ID: F####
- Run ID: {run-id}
- Date: YYYY-MM-DD
- Owner: DevOps / Feature Orchestrator

## Runtime Services / Containers / Jobs

Enumerate the runtime surfaces this feature touches: API services, workers, scheduled jobs, frontend dev server, AI runtime.

## Command Evidence

Document the preflight commands that brought the surface up locally. Cite `commands.log` lines.

```text
- docker compose up engine.api → healthy in 8s
- pnpm dev → port 5173 OK
```

## Health Status

Final status table:

| Service | Status | Notes |
|---------|--------|-------|
| engine.api | healthy | / |
| experience.web | healthy | / |

## Restore Steps If Unavailable

If a runtime surface cannot be brought up, document the recovery path and the operator runbook reference.

## Recommendations (when `WITH RECOMMENDATIONS`)

Each item uses the §15 canonical bullet:

```text
- [severity] <recommendation text> — owner: <name-or-role>; follow-up: <ticket-id-or-deferred-no-followup>
```

Severity is one of `low`, `medium`, `high`, `critical`. `high`/`critical` items require explicit PM mitigation per §15 PM Acceptance Line Format.

## Result

One of: `PASS`, `PASS WITH RECOMMENDATIONS`, `FAIL`.
