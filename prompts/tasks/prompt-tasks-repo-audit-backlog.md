<!-- Licensed under CC-BY 4.0. -->

# Repository Audit and BACKLOG.md Synthesis

## Purpose
Analyze the repository end to end and create or update a root-level BACKLOG.md with concise, non-duplicated, actionable items. Reconcile existing entries by marking resolved items as checked and avoiding duplicate unchecked items.

## Scope
- Code quality and architecture
- Tests and coverage
- Documentation (.md files, examples)
- CI/CD workflows
- Security and secrets hygiene
- Dependencies and build
- Release and changelog
- Repo hygiene and metadata

## Deliverables
1. BACKLOG.md at repo root, updated in place.
2. Pull request titled "Audit: update BACKLOG.md (code, docs, CI, security, deps)" summarizing counts of added, updated, and resolved items and linking to representative diffs.

## Audit Method
1. Inventory the repo:
   - Enumerate languages, projects, build tools, CI workflows, test projects, docs, scripts.
   - Detect TODO/FIXME tags, dead files, failing or missing tests, unused workflows, missing standard docs.
   - Inspect package and lock files for outdated or insecure dependencies.
   - Check for presence and basic quality of README, CONTRIBUTING, CODE_OF_CONDUCT, SECURITY, CHANGELOG, LICENSE, `.editorconfig`, `.gitattributes`, `.gitignore`.
   - Validate CI: existence, triggers, build matrix, caching, test execution, artifact publishing.
   - Check release hygiene: tags, versioning, changelog entries.
   - Review security hygiene: secret leaks in history, Dependabot/config, permissions in workflows.
2. Synthesize backlog items:
   - Only include items verifiable in the repo.
   - Each item fits one checkbox line with up to two short sub-bullets.
   - Prefer high-leverage items; assign priority P1, P2, or P3.
   - Provide evidence as file paths or workflow names; propose the smallest effective action.
3. Reconcile with existing BACKLOG.md:
   - Avoid duplicate unchecked items by canonicalizing titles.
   - Mark implemented unchecked items as checked with `(auto-checked on YYYY-MM-DD)`.
   - Preserve freeform notes outside checklist items.

## BACKLOG.md Format
- Title: `Backlog`
- Header metadata: `Last audit: YYYY-MM-DD`, `Added: N, Updated: M, Resolved: K`
- Legend: `Priorities: P1 critical, P2 important, P3 nice-to-have`
- Sections in this order, items sorted by priority then file path:
  1. Code quality and architecture
  2. Tests and coverage
  3. Documentation
  4. CI/CD
  5. Security
  6. Dependencies and build
  7. Release and changelog
  8. Repo hygiene and metadata
- Item schema:
  - `[P#][Area]` Short, action-oriented title
    - Why: brief rationale or impact
    - Evidence: file(s)/workflow(s) or commands to verify
- Checked items use `[x]` and keep their bullets.
- Link issues, PRs, or commits when available; prefer relative file links.

## Examples
- `[P1][Tests] Add unit test project for core library`
  - Why: public APIs lack coverage; reduces regression risk
  - Evidence: no test project found under `/tests`; CI does not run tests
- `[P2][CI] Enable caching for package restore to cut CI time`
  - Why: faster feedback loop and lower cost
  - Evidence: `.github/workflows/build.yml` has no cache steps
- `[P1][Security] Add secret scanning and Dependabot`
  - Why: detect leaks and automate updates
  - Evidence: no `.github/dependabot.yml`; no secret scanning badges
- `[P2][Docs] Expand README with quickstart and supported versions`
  - Why: onboarding clarity
  - Evidence: `README.md` missing install/build/usage sections
- `[P3][Hygiene] Add .editorconfig and enforce formatting`
  - Why: consistent code style
  - Evidence: `.editorconfig` not present

## Deduplication Rules
- Canonicalize titles: lowercase, strip punctuation, collapse spaces, remove stopwords `{the, a, an, to, for, of, and}`.
- Update existing items instead of adding near-duplicates.
- Do not remove user-authored prose outside checklist items.

## Validation
- Verify any resolved items by inspecting files or CI config.
- Do not mark items checked if verification is ambiguous.

## PR Requirements
- Single PR touching only `BACKLOG.md` unless trivial README typos are fixed.
- PR body includes:
  - Audit date
  - Counts: Added N, Updated M, Resolved K
  - Top 5 P1 actions with rationale
  - How to verify each proposed change

## Writing Constraints
- Checkbox titles ≤90 characters; sub-bullets ≤120 characters.
- Use clear, imperative voice; avoid marketing or speculation.
- Use consistent area tags: `[Code]`, `[Tests]`, `[Docs]`, `[CI]`, `[Security]`, `[Deps]`, `[Release]`, `[Hygiene]`.

## Acceptance Criteria
- `BACKLOG.md` exists at repo root and follows the format above.
- No duplicate unchecked items.
- Implemented items are checked with dated notes.
- Items are concise, actionable, and include Why and Evidence.
- PR created with required summary.

## Validation Checklist
- [ ] Repo inventory performed and backlog items synthesized.
- [ ] `BACKLOG.md` updated with metadata and deduplicated items.
- [ ] PR body summarizes counts and top P1 actions.
- [ ] Writing constraints and tags respected.
