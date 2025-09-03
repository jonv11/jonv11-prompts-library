# Weekly Maintenance Checklist

Use this checklist to keep the repository healthy on a weekly or bi-weekly cadence.

- Review dependency update PRs (Renovate/Dependabot) and pin versions.
- Run SCA/SAST and secret scans; triage and address findings.
- Lint and format the entire repository; ensure `.editorconfig` and `.gitattributes` are respected.
- Assess test health: flaky tests, coverage trends, and run a small mutation-testing sample.
- Check CI health: job durations, cache hit rate, flaky jobs, missing matrix targets.
- Triage `TODO`/`FIXME` tags and suppression comments.
- Sweep documentation for freshness (`README`, `CONTRIBUTING`, setup steps); test new-machine install.
- Link and spell check all docs; verify code snippets compile.
- Look for automation opportunities (e.g., Renovate/Dependabot, CodeQL, secret scanners, link checkers, spell checkers).
