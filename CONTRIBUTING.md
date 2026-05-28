# Contributing to Hermes SuperCode Skills

## Adding a New Skill

1. Create a directory under `skills/` with your skill name (lowercase-with-hyphens)
2. Write a `SKILL.md` following the structure below
3. Add trigger eval queries to `tests/trigger-eval.json`
4. Open a PR with a description of what the skill does and example usage

### SKILL.md Structure

```yaml
---
name: your-skill-name
description: |
  What the skill does and when it should trigger. Be specific about
  trigger patterns — list exact phrases users might say. Make the
  description slightly "pushy" to avoid under-triggering.
---
```

The body should include:
- **Identity** — one paragraph explaining the role
- **Workflow** — numbered phases the skill follows
- **Output format** — JSON schema for structured output
- **Safety rails** — red/yellow/green tier classification
- **Examples** — at least 2 realistic usage scenarios

### Quality Bar

- Keep SKILL.md under 500 lines
- Every workflow phase must be actionable (not just descriptive)
- Safety rails must cover destructive operations
- Output format must be valid JSON

## Modifying an Existing Skill

- Open an issue first to discuss the change
- Preserve the existing safety rails — relaxing them requires explicit justification
- Add test cases that cover your change
- Run the trigger eval to make sure your changes don't break triggering

## Trigger Evaluation

The `tests/trigger-eval.json` file contains queries that should and shouldn't
trigger each skill. Before submitting, verify your skill triggers correctly
on the should-trigger queries and doesn't trigger on the should-not queries.

## Code of Conduct

- No skills that facilitate unauthorized access to systems
- No skills that help bypass security measures
- No skills that collect or process PII without explicit user consent
- No skills that provide financial, medical, or legal advice as recommendations
