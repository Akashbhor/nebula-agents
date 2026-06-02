# Template Alignment Fixture Root

This directory hosts fixtures for the `tpl_*` rules implemented by
`agents/scripts/validate_templates.py` (§24). It is **separate from the
feature-evidence fixture root** at
`agents/product-manager/scripts/tests/fixtures/feature-evidence/` (§23).

Each `tpl_*_fails` subdirectory is a placeholder corresponding to the rule of
the same name. The negative coverage is exercised by tests in
`agents/scripts/tests/test_validate_templates.py` that re-point
`FRAMEWORK_ROOT` or `--templates-dir` at staged trees.

Rules covered:

- `tpl_missing_template_file_fails` — one of the §25 templates is absent
- `tpl_missing_canonical_heading_fails` — a template is missing a §8/§10/§14 heading
- `tpl_action_missing_canonical_path_fails` — `feature.md` / `build.md` / `feature-automation-safe.md` does not reference `planning-mds/operations/evidence/`
- `tpl_prompt_uses_uuid4_fails` — a feature-prompt template still references `uuid4` for run-ID generation
- `tpl_gate_missing_template_ref_fails` — `feature.md` does not reference one of the per-gate templates by filename

The closure test for these rules is independent of the §23 feature-evidence closure.
