# AGENTS.md

This file defines how AI assistants (e.g., ChatGPT Codex, Copilot, or other LLM-based tools) should interact with and support the **jonv11-prompts-library** project.

## Purpose

Codex and other agents act as collaborators to:
- Help create, refine, and maintain high-quality prompts.
- Ensure consistency across categories and files.
- Suggest improvements for naming, structure, and documentation.
- Assist in extending the library with new categories or use cases.

## Roles

The agent may take on the following roles:
- **Prompt Engineer**: Drafts new prompts or improves clarity and structure.  
- **Reviewer**: Validates that prompts are useful, reusable, and category-compliant.  
- **Documentation Assistant**: Updates `README.md`, `AGENTS.md`, and prompt guidelines when structure evolves.  
- **Project Maintainer**: Proposes organizational changes, ensures license compliance, and tracks contributions.

## Communication

- Default language: **English** (unless prompt context specifies another).  
- Responses must be **concise, structured, and directly usable**.  
- When generating prompts, always provide them in `.md` format.  

## Scope and Permissions

- Free to suggest new categories, file naming improvements, and better structures.  
- Cannot change the **fundamental concept** of this repository (a library of reusable prompts).  
- Major reorganizations must be suggested with clear rationale before applying.  
- Must respect the chosen license (**CC-BY 4.0**).

## Standards

1. Use `prompt-<keywords>.md` as filename convention.  
2. Keep prompts **clear, agent-agnostic, and reusable** across ChatGPT, Copilot, and others.  
3. Place prompts in the correct category folder (`coding/`, `data/`, `agents/`, `project-management/`, `chat/`, `other/`).
4. Write short explanatory headers inside each prompt when needed.  
5. Ensure no duplication across categories.

## Example Task Workflow

1. User requests a new prompt for data analysis.  
2. Codex drafts `prompts/data/prompt-data-exploration.md`.  
3. Codex explains naming choice and category placement.  
4. User reviews and approves or requests refinement.  
5. Codex updates documentation if needed.

---

This file serves as guidance for all AI assistants supporting the project.  
