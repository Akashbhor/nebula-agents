# Deployability Check — F####-{slug} run {run-id}

> Required per §10 for every completed terminal feature. DevOps or Feature Orchestrator owned.

## Runtime / Deployment Config Changes

Enumerate every changed Dockerfile, compose file, CI job, env-var contract, migration, startup script. If `deployment_config_changed = true`, this section is mandatory.

## Migrations / Rollback

Migration files added/altered, plus the rollback strategy. Cite the migration runner's output path.

## Env / Config Contract

Document every new or changed env var or config key. Note default values, secrets handling, and which environments are affected.

## Manifest Boolean Cross-Check

Confirm the manifest's `runtime_bearing`, `deployment_config_changed`, and `security_sensitive_scope` agree with what this report describes. Discrepancy is `scope_boolean_false_with_changed_paths_fails`.

## Build / Start / Smoke Results

Each artifact path resolves on disk or via cited URL.

```text
- build: docker compose build → exit 0 (artifacts/build/build.log)
- start: docker compose up -d → all services healthy
- smoke: scripts/smoke.sh → exit 0 (artifacts/smoke/smoke.log)
```

## Runtime Warnings

Non-blocking warnings to surface to the reviewer (deprecated config, expiring cert window, etc.).

## Recommendations (when `WITH RECOMMENDATIONS`)

§15 canonical bullet form. Severity `low`/`medium`/`high`/`critical`.

## Result

One of: `PASS`, `PASS WITH RECOMMENDATIONS`, `FAIL`.
