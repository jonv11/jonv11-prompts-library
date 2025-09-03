# Comprehensive Maintenance Checklist

Use this prompt when performing a full maintenance sweep. It combines weekly, monthly, release, and occasional tasks.

## Weekly Tasks
- Review dependency update PRs (Renovate/Dependabot) and pin versions.
- Run SCA/SAST and secret scans; triage and address findings.
- Lint and format the entire repository; ensure `.editorconfig` and `.gitattributes` are respected.
- Assess test health: flaky tests, coverage trends, and run a small mutation-testing sample.
- Check CI health: job durations, cache hit rate, flaky jobs, missing matrix targets.
- Triage `TODO`/`FIXME` tags and suppression comments.
- Sweep documentation for freshness (`README`, `CONTRIBUTING`, setup steps); test new-machine install.
- Link and spell check all docs; verify code snippets compile.

## Monthly Tasks
- Architecture review; update ADRs and diagrams; examine the dependency graph for tangles.
- Remove dead code and unused modules; plan deprecations; audit public API surface.
- Capture performance baselines and detect regressions on key paths.
- Perform a supply chain audit: build an SBOM, check license compliance, update third-party notices.
- Verify lockfiles and reproducible builds; ensure deterministic outputs.
- Check configuration and infrastructure drift across environments; maintain parity of flags and defaults.
- Review access: tokens, keys, secret rotation, least-privilege policies.
- Confirm ownership accuracy: `CODEOWNERS`, runbooks, on-call docs.
- Ensure cross-repo consistency: PR/issue templates, commit message rules, branching model.

## Release Tasks
- Verify versioning and `CHANGELOG` updates; confirm semantic version bump.
- Provide migration notes and deprecation warnings where needed.
- Execute a clean-room build and run E2E and smoke tests on all target OS/architectures.
- Perform packaging checks: signing, attach SBOM, ensure license headers.
- Finalize release notes; regenerate and publish the docs site.

## Occasional Tasks
- Update threat model and data-flow diagrams.
- Run backup and restore drills if data is involved.
- Expand benchmark suite and test datasets.
- Check privacy and retention policy compliance.

## Automation
- Leverage tools like Renovate/Dependabot, CodeQL or equivalent, secret scanners, link and spell checkers, doc snippet compilers, flaky-test detectors, coverage gating, and release CI with changelog generation wherever possible.
