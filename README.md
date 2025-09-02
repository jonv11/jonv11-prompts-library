# jonv11-prompts-library

A structured library of reusable AI prompts for ChatGPT, Copilot, and other LLM-based agents.  
The goal is to keep prompts organized, portable, and ready to use across coding, documentation, data analysis, creative tasks, and project management.

## Structure

```
jonv11-prompts-library/
├── AGENTS.md
├── CHANGELOG.md
├── CONTRIBUTING.md
├── LICENSE
├── README.md
└── prompts/
    └── projects/
        └── prompt-update-docs.md
```

The library organizes prompts by category. Currently only the `projects/` folder is populated, but additional folders can be added as the library grows:

- **coding/**: prompts for code generation, debugging, optimization.
- **data/**: prompts for analysis, visualization, entity resolution, statistics.
- **agents/**: prompts defining AI agent roles, behaviors, workflows.
- **chat/**: prompts for conversational use, fact-checking, Q&A.
- **other/**: prompts that don’t fit the main categories.
- **projects/**: prompts for project initiation, planning, specs, docs.

Each prompt is a standalone `.md` file with:
- **Descriptive filename** (e.g., `prompt-code-review.md`).  
- **Readable description** of the goal and expected output.  
- **Clear structure** so it works in ChatGPT, Copilot, or similar.

## Usage

1. Browse `prompts/<category>/` for what you need.  
2. Copy the content of the `.md` file into your AI tool (ChatGPT, Copilot, etc.).  
3. Adapt inputs as required by the prompt.

## Contribution

- Keep prompts short, clear, and generic enough to be reused.
- Use English as default language unless the prompt specifies otherwise.
- Follow the naming pattern: `prompt-<keywords>.md`.
- Place in the correct category subfolder.
- Add documentation when needed.

See [CONTRIBUTING.md](CONTRIBUTING.md) for full guidelines.

## License

This repository is licensed under **CC-BY 4.0**, which means prompts can be reused and adapted with attribution.

