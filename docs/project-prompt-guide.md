# Project Prompt Guide

Use ChatGPT's **Projects** feature to share persistent instructions and files across conversations. A project acts as a workspace where uploaded code, docs, and notes are available to every chat started within the project.

## Setup

- **Upload context files**: Add key docs like `README.md`, `AGENTS.md`, and relevant source files so the assistant can reference them.
- **Project instructions**: Set high-level guidelines—style rules, build steps, or goals—that apply to all chats in the project.
- **Organize files**: Maintain a clear structure so paths are predictable.

## Prompting Strategies

- **Mention exact paths**: Refer to specific files or directories when making requests.
- **Describe desired changes**: Provide goals, acceptance criteria, and edge cases.
- **Quote relevant snippets**: Include line numbers or code blocks to focus edits.
- **Request commands**: Ask the assistant to run build or test commands after changes.
- **Iterate**: Break large tasks into smaller prompts and review results incrementally.
- **Update context**: Refresh project instructions or files when dependencies change.

## Collaboration Tips

- **Keep project files current** so future chats use accurate context.
- **Use version control**: Commit small, atomic changes for easy review and rollback.
- **Verify outputs**: Run tests and inspect diffs before merging.
