# Guide to Creating Effective Prompts (ChatGPT & Codex)

## Introduction

Clear prompts yield better results. This document gives best practices, must-haves, and to-dos for two cases: conversational prompts for ChatGPT and coding tasks for Codex. It also explains how to store prompts in a repository and how to use `AGENTS.md` or `.github/copilot-instructions.md` to guide coding agents.

## General Best Practices for Prompt Content

- Lead with the ask. Put the instruction first. Separate instructions from any background using clear delimiters (triple quotes or fenced blocks).
- Be specific. Define desired outcome, scope, length, format, style, constraints, and success criteria.
- Provide only relevant context. Include the minimum background needed. Delimit it so it cannot be confused with instructions.
- Show the format. Provide a target structure or example output (e.g., JSON schema, headings, bullet template).
- Encourage step-by-step work. For multi-step problems, ask for numbered reasoning or list the steps to follow.
- Prefer positive guidance. Tell what to do, not only what to avoid. If something is forbidden, give the alternative behavior.
- Avoid ambiguity or conflicting asks. Split unrelated goals into separate sections or separate prompts.
- Set tone and perspective. State role, audience, and voice when it matters.
- Use few-shot only when needed. Provide 1–3 clean, correct examples to teach a format or pattern.
- Respect context limits. Keep prompts concise and scannable. Use headings and bullets.

## Crafting Prompts for ChatGPT (Conversational Tasks)

- Establish role or scenario when useful (“You are an expert X…”).
- Ask direct questions or commands.
- Include source text or data when required, clearly separated from the instruction.
- Specify output format and length (bullets, steps, short summary, multi-section brief, JSON, etc.).
- Set tone and style (friendly, technical, formal).
- Avoid vague, open-ended asks if you need precision; narrow the angle.
- Test and iterate by refining wording based on results.

## Crafting Prompts for Codex (Coding Tasks)

- Point to specific code: file paths, functions, errors, or stack traces.
- Include verification steps: how to build, run, test, or lint; define “done” (tests pass, CLI output equals X).
- State constraints and preferences: patterns, APIs, performance vs readability, allowed files to change.
- Break down large tasks into sub-steps; optionally ask Codex to outline then implement step 1 first.
- Provide failing cases or logs for debugging tasks.
- Use lead-ins to set language/mode (e.g., start with a comment and import for Python, SELECT for SQL).
- Leverage Codex for design and review: request edge cases, refactors, or documentation.
- Maintain context across turns by re-referencing function and file names if chat memory is limited.

## Organizing Reusable Prompts in a Repository

- One prompt per file in Markdown.
- Use clear, descriptive names like `prompt-summarize-report.md`, `prompt-generate-unit-tests.md`.
- Group logically under `prompts/`, with subfolders by tool or use case when the library grows.
- Add brief usage notes at top of each file or in a folder README (clearly marked as not part of the prompt).
- Version control prompts like code; commit messages explain changes.
- Optimize for copy-paste: avoid extra boilerplate that should not be fed to the model.
- Reference the library from the main README so others can discover and reuse prompts.

## Using AGENTS.md and Copilot Instruction Files

Modern coding agents read repository instructions to operate effectively.

### What to provide

- Project overview: purpose and tech stack.
- Environment & commands: build, run, test, lint, and prerequisites.
- Testing policy: how to run tests; expectations for new tests.
- Code style and conventions: formatting, patterns, commit message rules, architectural constraints.
- Repository structure: where things live; where to add new code.
- Security and policy: secrets handling, disallowed libs, approved crypto, compliance notes.

### File locations supported

- `AGENTS.md` at repo root (preferred, broadly supported).
- `.github/copilot-instructions.md` (GitHub-specific) and path-scoped instruction files when different areas need different rules.

### Writing style

- Keep it concise, skimmable, and imperative. Use headings and bullets.

### Granularity

- One top-level instructions file is often enough. Add path-specific files for heterogeneous repos with different build/test flows.

### Benefits

- Agents build, test, and validate in-context, producing changes that better match your project and reduce review time.

### Minimal example (illustrative)

#### Build & Test

- Build: run your documented build command.
- Test: run your documented test command; all tests must pass.
- Lint/format: run the repo’s linters/formatters before proposing changes.

#### Coding Conventions

- Follow the project’s style guide.
- Add or update tests for new behavior.
- Use semantic commit messages.

#### Repository Structure

- Briefly map the main folders and where to place new code.

## Conclusion

Well-structured prompts improve accuracy and efficiency. Treat prompts as first-class artifacts: clear instructions, minimal but sufficient context, explicit formats, and verification steps. Store prompts as Markdown, version them, and guide coding agents with AGENTS.md or Copilot instructions for build/test/style/structure so automated changes align with your codebase.

## Sources and Further Reading

- OpenAI Prompt Engineering best practices.
- OpenAI Codex prompting guide.
- Prompt design guidelines from the community.
- AGENTS.md standard overview and GitHub Copilot changelog on custom instructions.
- GitHub Copilot docs on getting the best results from the coding agent.

