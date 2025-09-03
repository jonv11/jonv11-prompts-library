# Backlog

Last audit: 2025-09-03
Added: 12, Updated: 0, Resolved: 0

Priorities: P1 critical, P2 important, P3 nice-to-have

## Code quality and architecture
- [ ] [P1][Code] Add Markdown linting for prompt files
  - Why: maintain consistent style and catch formatting errors
  - Evidence: no `.markdownlint` config (`find . -maxdepth 2 -name '.markdownlint*'`)

## Tests and coverage
- [ ] [P1][Tests] Add automated validation for prompt markdown
  - Why: detect broken links and guideline regressions
  - Evidence: `npm test` fails; no `package.json`

## Documentation
- [ ] [P2][Docs] Add CODE_OF_CONDUCT.md
  - Why: set community behavior expectations
  - Evidence: no `CODE_OF_CONDUCT.md` in repo root
- [ ] [P3][Docs] Update README project tree to list all docs files
  - Why: avoid confusion from outdated structure
  - Evidence: `README.md` lists only one file under `docs/`

## CI/CD
- [ ] [P1][CI] Add GitHub Actions workflow to run lint and tests
  - Why: enforce quality checks on commits
  - Evidence: no workflows (`find . -path '.github/workflows/*.yml'`)

## Security
- [ ] [P1][Security] Add SECURITY.md and enable secret scanning
  - Why: define vulnerability reporting and detect leaks
  - Evidence: no `SECURITY.md` or secret scanning setup
- [ ] [P2][Security] Configure Dependabot for GitHub Actions and packages
  - Why: keep dependencies patched automatically
  - Evidence: no `.github/dependabot.yml`

## Dependencies and build
- [ ] [P3][Deps] Initialize package manifest and scripts for tooling
  - Why: manage future lint and test dependencies
  - Evidence: `npm test` error `ENOENT: no such file or directory, open 'package.json'`

## Release and changelog
- [ ] [P2][Release] Introduce semantic version tags and release workflow
  - Why: track versions and communicate changes
  - Evidence: no git tags; `CHANGELOG.md` only has Unreleased

## Repo hygiene and metadata
- [ ] [P1][Hygiene] Add `.gitignore` to exclude temporary files
  - Why: prevent committing artifacts or editor files
  - Evidence: no `.gitignore` (`find . -name '.gitignore'`)
- [ ] [P2][Hygiene] Add `.editorconfig` for consistent formatting
  - Why: standardize indentation and line endings
  - Evidence: no `.editorconfig` in repository
- [ ] [P3][Hygiene] Add `.gitattributes` for text normalization
  - Why: ensure consistent diffs across platforms
  - Evidence: no `.gitattributes` present
