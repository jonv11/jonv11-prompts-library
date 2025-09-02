# Creating Effective Prompts for GitHub Copilot

This guide explains how to steer GitHub Copilot within your editor to produce useful code suggestions.

## Key Context Files

Copilot draws context from your workspace to craft completions:

- **Open file around the cursor** – primary source for style and intent.
- **Neighboring files and imports** – help Copilot infer APIs and patterns.
- **README.md and other docs** – provide project goals and usage examples.
- **Build and dependency configs** (e.g., `package.json`, `pyproject.toml`) – reveal frameworks, scripts, and versions.
- **Tests and example files** – show expected behavior and edge cases.
- **Lint and formatting configs** – influence stylistic choices like tabs or semicolons.

## Crafting Prompts

- **Write descriptive comments** before functions or blocks to explain desired behavior.
- **Name functions and variables clearly** to signal intent.
- **Provide small scaffolds** such as TODOs, signature stubs, or sample inputs.
- **Specify output structure** in comments or docstrings when necessary.
- **Iterate** by accepting, editing, or rejecting suggestions to guide future completions.

## Best Practices

- **Keep context files accurate** so Copilot bases suggestions on the latest code.
- **Add unit tests** to reinforce expected behavior and guide completions.
- **Review generated code** for security, performance, and licensing before committing.
