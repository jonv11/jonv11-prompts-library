<!-- Licensed under CC-BY 4.0. -->

# Weekly Maintenance Checklist

## Purpose
Keep the repository healthy on a weekly or bi-weekly cadence.

## Steps
- Review dependency update PRs (Renovate/Dependabot) and pin versions.
- Run SCA/SAST and secret scans; triage and address findings.
- Lint and format the entire repository; ensure `.editorconfig` and `.gitattributes` are respected.
- Assess test health: flaky tests, coverage trends, and run a small mutation-testing sample.
- Check CI health: job durations, cache hit rate, flaky jobs, missing matrix targets.
- Triage `TODO`/`FIXME` tags and suppression comments.
- Sweep documentation for freshness (`README`, `CONTRIBUTING`, setup steps); test new-machine install.
- Link and spell check all docs; verify code snippets compile.
- Look for automation opportunities (e.g., Renovate/Dependabot, CodeQL, secret scanners, link checkers, spell checkers).

## Output
- Notes on actions taken and any follow-up items.

## Acceptance Criteria
- Each task reviewed and addressed.
- Tests, scans, and linters run where applicable.
- Follow-up tasks documented.

## Validation Checklist
- [ ] Dependency updates reviewed.
- [ ] Security scans and linters executed.
- [ ] Documentation refreshed and checked.
- [ ] Automation opportunities logged.
