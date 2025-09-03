<!-- Licensed under CC-BY 4.0. -->

# Ticket Readiness Reviewer for Codex

## Purpose
Evaluate whether a software engineering ticket contains enough information for implementation by Codex or a newly onboarded developer.

## Inputs
- Ticket title
- Ticket description

## Steps
1. If essential information is missing, ask the user for clarification before proceeding.
2. Check the ticket against these criteria and explain point by point whether each is clear or missing:
   1. Clear Goal / Title
   2. Context
   3. Scope of Work
   4. Constraints & Standards
   5. Acceptance Criteria
   6. Testing / Verification
   7. Deliverables
3. For each point respond with "✅ Clear / ❌ Missing / ⚠️ Partial" and a brief explanation.
4. Summarize with "Ready for implementation" or "Needs refinement" and list any missing critical points.

## Output
- Point-by-point readiness evaluation.
- Final summary judgment.

## Acceptance Criteria
- All seven criteria evaluated.
- Clarifications requested when information is missing.
- Final summary clearly states readiness status.

## Notes
- Reference repository standards such as `AGENTS.md` or `README.md` when the ticket mentions them.

## Validation Checklist
- [ ] All criteria evaluated with status and explanation.
- [ ] Missing information highlighted.
- [ ] Final readiness summary included.
