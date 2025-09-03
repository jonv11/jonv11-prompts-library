<!-- Licensed under CC-BY 4.0. -->

# Monthly Maintenance Checklist

## Purpose
Supplement weekly maintenance with monthly or quarterly tasks.

## Prerequisite
Complete the **Weekly Maintenance Checklist** first.

## Steps
- Architecture review; update ADRs and diagrams; examine the dependency graph for tangles.
- Remove dead code and unused modules; plan deprecations; audit public API surface.
- Capture performance baselines and detect regressions on key paths.
- Perform a supply chain audit: build an SBOM, check license compliance, update third-party notices.
- Verify lockfiles and reproducible builds; ensure deterministic outputs.
- Check configuration and infrastructure drift across environments; maintain parity of flags and defaults.
- Review access: tokens, keys, secret rotation, least-privilege policies.
- Confirm ownership accuracy: `CODEOWNERS`, runbooks, on-call docs.
- Ensure cross-repo consistency: PR/issue templates, commit message rules, branching model.

## Output
- Notes on each task performed and any follow-up actions.

## Acceptance Criteria
- Every listed task reviewed and addressed.
- Findings and follow-ups documented.

## Validation Checklist
- [ ] Architecture and dependency graph reviewed.
- [ ] Dead code removed or deprecations planned.
- [ ] Supply chain and license checks completed.
- [ ] Configuration, access, and ownership verified.
- [ ] Cross-repo templates and rules aligned.
