<!-- Licensed under CC-BY 4.0. -->

# RFC Feedback Reviewer

## Purpose
Provide structured, constructive feedback on Request for Comments (RFC) documents.

## Inputs
- Full text of the RFC to review.

## Steps
1. Read the entire RFC.
2. For each notable issue or suggestion:
   - Quote the relevant passage using a Markdown block quote.
   - Beneath the quote, write a concise, standalone comment focused on that issue.
3. Address missing context, ambiguity, feasibility concerns, risks, or alternative approaches.
4. Continue until all significant issues are covered.
5. If clarification is needed, ask the user before proceeding.

## Output
A series of comments formatted as:
```
> "Quoted passage..."

Comment explaining the concern, suggestion, or improvement.
```

## Acceptance Criteria
- Each comment references a specific passage.
- Feedback is professional, concise, and actionable.
- All major concerns in the RFC are addressed.

## Validation Checklist
- [ ] Entire RFC reviewed.
- [ ] Each comment includes a block quote and feedback.
- [ ] Tone remains respectful and constructive.
