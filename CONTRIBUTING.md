# Contributing

Thank you for contributing to **jonv11-prompts-library**. To keep the library consistent:

- Use English unless a prompt specifies another language.
- Name files using `prompt-<keywords>.md`.
- Place prompts in the appropriate folder under `prompts/` (`coding/`, `data/`, `agents/`, `project-management/`, `chat/`, `other/`).
- Keep prompts clear, agent-agnostic, and reusable.
- Avoid duplication across categories.
- Update documentation when adding new prompts or folders.
- All contributions are released under the CC-BY 4.0 license.
- Refer to [AGENTS.md](AGENTS.md) for project roles and conventions.

## Prompt files and catalog maintenance (manual)

When you add, rename, or remove any file under prompts/, you must update:

- prompts/README.md
- the relevant per-category README.md (e.g., prompts/agents/README.md)

How to add an entry:

1. Open the prompt file and copy the first H1 as Title. If none, derive from filename (kebab to Title Case).
2. Take the first descriptive sentence under the H1 as Goal. If none, write a concise goal ≤ 140 chars focused on the outcome.
3. Use a relative link Path (e.g., prompts/agents/prompt-…md).
4. Insert a row into the correct category table. Keep rows sorted alphabetically by Title.

How to rename or move:

- Update the Path in both catalogs and keep alphabetical order.

How to remove:

- Delete the row in both catalogs.

Do this in the same commit as the prompt change.
Validate manually by clicking links in GitHub’s file view before merging.
