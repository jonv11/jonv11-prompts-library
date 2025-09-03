<!-- Licensed under CC-BY 4.0. -->

# Repository Bootstrap Prompt

## Purpose

Guide a user through bootstrapping a new GitHub repository using widely accepted standards. Ask for goals and preferences, then output a Codex task snippet that produces ready-to-commit files and structure. Remain agent-agnostic and compatible with ChatGPT and GitHub Copilot/Codex.

## Inputs

- Repository name: taken from the agent/task context or asked if missing.
- Short description: one sentence for README and repo tagline.
- Primary language/stack: e.g., “Node.js”, “Python”, “Scala/Spark”.
- License: choose at run time (MIT, Apache-2.0, GPL-3.0, BSD-3-Clause, CC-BY-4.0, Unlicense). Provide guidance.
- Visibility: public or private.
- Initial scope/goals: 2–5 bullets.
- CI preference: none or GitHub Actions starter.
- Issue templates: enable bug/feature templates? yes/no.
- PR template: yes/no.
- Changelog policy: keep a CHANGELOG.md? yes/no.
- Contributor policy: include CONTRIBUTING.md? yes/no.
- Code of conduct: include CODE_OF_CONDUCT.md? yes/no.
- Security policy: include SECURITY.md? yes/no.
- Editor settings: include .editorconfig and .gitattributes? yes/no.
- Ignore rules: include language-appropriate .gitignore? yes/no.
- Owners/routing: include CODEOWNERS? yes/no.
- Prompt library compatibility: create `prompts/` folder skeleton? yes/no.

## Steps

1. Seed an empty repository:
   - If no files exist yet, create a temporary `README.md` so Codex tasks don’t fail
     on an empty repo.
   - The generated bootstrap snippet may safely overwrite this file if it is the only
     file present.
2. Clarify repository goal:
   - Ask for short description and 2–5 scope bullets.
   - Confirm primary language/stack and visibility.
3. Explain standard files and let the user opt in/out. For each item below, show a one-line purpose and recommended default:
    - `README.md` (recommended): Project overview, quickstart, structure, license badge.
    - `LICENSE` (required by choice): Legal reuse terms. Briefly explain common options:
      - MIT: permissive, simple.
      - Apache-2.0: permissive with patent grant.
      - GPL-3.0: copyleft, derivative works must be GPL.
      - BSD-3-Clause: permissive, attribution, non-endorsement.
      - CC-BY-4.0: content/docs licensing with attribution (not ideal for code).
      - Unlicense: public domain dedication.
    - `CONTRIBUTING.md` (recommended for collaboration): How to propose changes, branching, commit style.
    - `CODE_OF_CONDUCT.md` (recommended for public repos): Community expectations and reporting.
    - `SECURITY.md` (recommended for public repos): How to report vulnerabilities; supported versions.
    - `CHANGELOG.md` (optional but common): Human-readable changes per release; keepers: Keep a Changelog style.
    - `.gitignore` (recommended): Language/framework ignores based on the chosen stack.
    - `.gitattributes` (recommended): EOL normalization, linguist overrides for docs/examples.
    - `.editorconfig` (recommended): Consistent whitespace, charset, indent size.
    - `.github/ISSUE_TEMPLATE/bug_report.md` (optional): Standard bug intake fields.
    - `.github/ISSUE_TEMPLATE/feature_request.md` (optional): Standard feature intake fields.
    - `.github/PULL_REQUEST_TEMPLATE.md` (optional): Checklist and summary for PRs.
    - `.github/workflows/ci.yml` (optional): Minimal CI template for chosen stack.
    - `CODEOWNERS` (optional): Auto-assign reviewers.
    - `prompts/` (optional): For prompt libraries. Add `prompts/README.md` and `.keep`.
4. Collect run-time choices and generate a plan table: file → include? → reason.
5. Build a Codex task snippet that creates the chosen files with appropriate content. Include path, description, and summarized content guidance for each task.
6. Output:
   - A tree view of files to add.
   - Codex task snippet.
   - Suggested commit messages.
   - Next steps checklist.
7. Validate with the checklist below before final answer.

## Output

- “Planned files” table with inclusion decisions and rationale.
- Repository tree preview.
- Codex task snippet for generating files.
- Suggested commit message, e.g.: `chore: bootstrap repository with standard files`.
- Reminder to follow `CONTRIBUTING.md` and run any tests or linters if defined.

## Acceptance Criteria

- Uses only widely accepted GitHub-standard files and placements.
- Explains each optional file succinctly and lets the user opt in/out.
- License is chosen at run time with clear guidance; correct boilerplate is produced.
- Outputs valid Markdown/YAML/text with correct paths.
- CI template matches the declared primary stack if selected.
- Prompts folder (if selected) follows `prompt-<keywords>.md` naming and English wording.
- Final answer includes tree, Codex task snippet, and commit message suggestions.

## Metadata

- tags: repository, bootstrap, github, standards, documentation
- target: ChatGPT, GitHub Copilot/Codex
- language: English

## Notes

- Prefer official GitHub templates where applicable.
- Keep texts concise and professional.
- Do not add niche or organization-specific files by default.
- For brand-new repositories, create and commit a placeholder `README.md` before
  running Codex tasks. The bootstrap snippet may replace it if `README.md` is the
  only existing file.

## Validation Checklist

- [ ] All included files are standard and placed under correct paths.
- [ ] License text matches the selected license exactly.
- [ ] README includes description, quickstart, structure, contributing, license note.
- [ ] Templates and CI syntax validate.
- [ ] `.editorconfig`, `.gitattributes`, `.gitignore` align with the selected stack.
- [ ] Optional `prompts/` follows repository rules and naming.
