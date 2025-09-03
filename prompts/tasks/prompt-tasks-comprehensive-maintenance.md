<!-- Licensed under CC-BY 4.0. -->

# Comprehensive Maintenance Checklist

## Purpose
Perform a full maintenance sweep combining weekly, monthly, release, and occasional tasks.

## Steps
### Weekly Tasks
- Review dependency update PRs and pin versions.
- Run SCA/SAST and secret scans; triage and address findings.
- Lint and format the repository; ensure `.editorconfig` and `.gitattributes` are respected.
- Assess test health: flaky tests, coverage trends, and a small mutation-testing sample.
- Check CI health: job durations, cache hit rate, flaky jobs, missing matrix targets.
- Triage `TODO`/`FIXME` tags and suppression comments.
- Sweep documentation for freshness; test new-machine install.
- Link and spell check docs; verify code snippets compile.

### Monthly Tasks
- Architecture review; update ADRs and diagrams; examine dependency graph for tangles.
- Remove dead code and unused modules; plan deprecations; audit public API surface.
- Capture performance baselines and detect regressions on key paths.
- Perform a supply chain audit: build an SBOM, check license compliance, update third-party notices.
- Verify lockfiles and reproducible builds.
- Check configuration and infrastructure drift across environments.
- Review access: tokens, keys, secret rotation, least-privilege policies.
- Confirm ownership accuracy: `CODEOWNERS`, runbooks, on-call docs.
- Ensure cross-repo consistency: templates, commit rules, branching model.

### Release Tasks
- Verify versioning and `CHANGELOG` updates; confirm semantic version bump.
- Provide migration notes and deprecation warnings where needed.
- Execute a clean-room build and run E2E and smoke tests on all target OS/architectures.
- Perform packaging checks: signing, attach SBOM, ensure license headers.
- Finalize release notes; regenerate and publish the docs site.

### Occasional Tasks
- Update threat model and data-flow diagrams.
- Run backup and restore drills if data is involved.
- Expand benchmark suite and test datasets.
- Check privacy and retention policy compliance.

## Output
- Confirmation that each checklist item was reviewed and addressed.
- Notes for follow-up actions.

## Acceptance Criteria
- All tasks reviewed and actions noted.
- Tests, linters, and scans run where applicable.
- Documentation and configuration remain current.

## Validation Checklist
- [ ] Dependency updates and security scans completed.
- [ ] Documentation, configurations, and ownership verified.
- [ ] Release and occasional tasks checked as needed.
- [ ] Follow-up issues logged for any gaps.
