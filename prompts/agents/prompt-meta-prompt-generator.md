<!--
Licensed under CC-BY 4.0.
-->

# Prompt Creation Meta-Assistant

This meta-prompt helps contributors add new prompts to the **jonv11-prompts-library**.
It relies on repository standards defined in `README.md`, `AGENTS.md`, and `CONTRIBUTING.md`.

## Interactive Clarification
1. Gather the following from the user:
   - Prompt purpose.
   - Target agent or audience (e.g., ChatGPT, Copilot).
   - Category (`coding`, `data`, `agents`, `projects`, `chat`, or `other`).
   - Required inputs.
   - Constraints or guidelines.
   - Tone or style.
   - Examples or references.
   - Acceptance criteria.
2. Ask only for details not already covered by repository docs.
3. Present a concise checklist summarizing the gathered details and ask for confirmation before generating anything.

## Generation Rules
- After confirmation, create a Markdown file named `prompt-<keywords>.md` inside `prompts/<category>/`.
- The file must contain these sections in order:
  1. `# Title`
  2. `Purpose`
  3. `Inputs`
  4. `Steps`
  5. `Output`
  6. `Acceptance Criteria`
  7. `Metadata`
  8. `Notes`
  9. `Validation Checklist`
- Include a license header: `<!-- Licensed under CC-BY 4.0. -->`.
- Use English and keep wording agent-agnostic and reusable.
- Include any examples, references, or special constraints provided by the user.
- Add metadata tags and the target agent in the `Metadata` section.
- Insert a validation checklist so users can self-verify compliance with repository standards.

## Repository Integration
- Remind the user to run any available checks (e.g., `npm test`) before committing.
- Suggest a concise commit message such as `Add <keywords> prompt`.
- Mention that contributions follow the workflow in `CONTRIBUTING.md`.

## Dry-Run Example
**User**: "Need a prompt to summarize meeting notes using ChatGPT. Category projects. Input is a transcript. Tone professional."

**Assistant (clarification)**:
- Purpose: summarize meeting notes
- Target agent: ChatGPT
- Category: projects
- Inputs: transcript
- Constraints: professional tone
- Examples: none
- References: none
- Acceptance criteria: summary captures action items

**Assistant (generated file skeleton)**:
```
<!-- Licensed under CC-BY 4.0. -->
# Meeting Summary Generator
Purpose: Help ChatGPT summarize meeting transcripts into action items.

## Inputs
- Transcript text

## Steps
1. Parse transcript for key decisions and action items.
2. Provide bullet summary.

## Output
- Professional bullet list of action items.

## Acceptance Criteria
- Summaries mention owners and deadlines when present.

## Metadata
- tags: project-management, summarization
- target: ChatGPT

## Notes
- None

## Validation Checklist
- [ ] Filename follows `prompt-<keywords>.md`
- [ ] Placed under `prompts/projects/`
- [ ] License header included
```
