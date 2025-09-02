# Creating Effective Prompts for OpenAI Codex

This guide summarizes best practices for working with OpenAI Codex to maintain repositories and design prompts. Codex acts as a cloud-based coding agent that can read and modify your repository, run tests, and propose pull requests.

## Key Context Files

Codex inspects several files to understand your project before acting:

- **AGENTS.md** – rules for agent behavior, build commands, and style expectations.
- **README.md** – overview, setup notes, and usage examples that frame tasks.
- **Build and dependency configs** (e.g., `package.json`, `.csproj`) – reveal languages, scripts, and required tools.
- **Tests** – show expected behavior and regression safeguards.
- **Linting and formatting configs** – enforce style and quality gates.
- **Environment examples** (like Docker files) – document how to reproduce the setup.

## Crafting Prompts

- **Be clear and specific**: Describe the exact change or question. Reference files or functions directly and include code snippets when helpful.
- **Provide context**: Mention related modules or existing issues so Codex focuses on the right areas.
- **Use an instructional tone**: Frame prompts as direct tasks or commands with acceptance criteria.
- **State goals**: Explain success conditions such as performance targets or test expectations.
- **Keep tasks focused**: Break large requests into smaller sequential steps.
- **Iterate**: Review Codex's output, then refine prompts or request follow‑up changes.
- **Leverage Q&A mode**: Ask Codex about codebase details before assigning modifications.

## Preparing the Repository

- Keep **AGENTS.md** and **README.md** current so Codex receives accurate instructions.
- Ensure build and dependency files reflect supported languages and scripts.
- Maintain a comprehensive test suite and document how to run it.
- Include linting and formatting configs plus pre‑commit hooks to enforce style.
- Provide environment examples (Docker files, `.env` templates) to reproduce the setup.

## Delegating Tasks to Codex

Codex can automate many maintenance activities:

1. **Update dependencies** and adjust code for compatibility, running tests afterward.
2. **Fix bugs** by describing symptoms and expected behavior; request accompanying tests.
3. **Implement features** by outlining modules, functions, and integration points.
4. **Refactor code** with goals like reducing duplication while preserving behavior.
5. **Revise documentation** such as README updates or code comments.

## Limitations and Best Practices

- **Review outputs** as you would a junior developer's work and run tests independently.
- **Provide sufficient context** for very large repositories or multiple services.
- **Plan prompts carefully** since mid‑task corrections are not possible.
- **Monitor task duration and usage limits**; break up long‑running jobs.
- **Consider privacy and security** when running Codex on sensitive code or with internet access.
- **Rely on CI and test suites** to validate changes before merging.
- **Refine AGENTS.md and docs** to align Codex with project standards.

By supplying clear instructions, maintaining thorough documentation, and using a robust test suite, you can delegate routine repository tasks to Codex with confidence.

