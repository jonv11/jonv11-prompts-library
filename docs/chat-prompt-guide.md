# Simple Chat Prompt Guide

This guide covers prompt crafting for chat interfaces like ChatGPT or Copilot where only the prompt text is available.

## Strategies

- **Establish a role**: Set the assistant's persona or expertise at the start.
- **Deliver necessary background**: Include all context the model needs since no external files are loaded.
- **Ask direct questions or tasks**: Keep requests focused and unambiguous.
- **Specify format and tone**: Indicate if the response should be concise, formal, or in a specific structure.
- **Encourage step-by-step reasoning**: Request explanations or intermediate steps for clarity.
- **Use delimiters for code or data**: Fence code blocks with backticks to preserve formatting.
- **Set boundaries**: Mention length limits, forbidden topics, or required citations.

## Managing Dialog

- **Reference prior messages** when continuing a conversation to maintain context.
- **Summarize progress** if the thread becomes long so the assistant stays on track.
- **Invite clarifying questions** when the task may be misunderstood.
