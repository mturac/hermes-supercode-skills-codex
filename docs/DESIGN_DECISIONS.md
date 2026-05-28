# Design Decisions

This document explains the architectural choices behind Hermes SuperCode Skills.

## Why Claude Code Skills?

Claude Code skills are the most straightforward way to give Claude domain
expertise that persists across sessions. A SKILL.md file in the right
directory is automatically available — no API keys, no server, no build step.

## Structural Choices

### Every skill follows the same workflow pattern

Recon → Plan → Execute → Verify (with variations per domain). This
consistency means users who learn one skill's rhythm can predict how
the others work. It also means skills can compose — mcp-conductor can
orchestrate other skills because they all follow the same phase structure.

### No shared dependencies between skills

Each skill is self-contained. You can install one skill or all ten.
No skill imports from another, no shared configuration file, no global
state. This makes maintenance straightforward and allows independent
versioning.

### Safety rails are tiered, not binary

Every skill uses a three-tier safety model:

- **Red (never do):** actions that are dangerous regardless of context
- **Yellow (confirm first):** actions that are usually fine but need
  explicit user consent
- **Green (safe):** actions that can be executed without asking

This avoids both the "ask permission for everything" antipattern (which
trains users to click "yes" without reading) and the "YOLO" antipattern
(which leads to production incidents).

### Structured JSON output

Every skill produces machine-parseable JSON output. This serves two
purposes: (1) the user gets a structured summary they can pipe into
other tools, and (2) the mcp-conductor skill can consume output from
other skills programmatically.

### Skills stay under 500 lines

Following Claude Code skill best practices, each SKILL.md is kept under
500 lines. This ensures the full skill fits comfortably in context. For
skills that need deep reference material (security-sentinel's OWASP
mappings, api-sculptor's OpenAPI examples), use the `references/`
directory for progressive disclosure.

## What's NOT in this collection

- **No custom runtime** — these are plain SKILL.md files, not a framework
- **No shared state** — skills don't persist data between invocations
- **No proprietary model requirement** — works with any model Claude Code
  supports
- **No external API dependencies** — skills describe methodology, the user
  provides their own API keys where needed

## Naming Conventions

Skill names are lowercase-with-hyphens, matching the directory name.
Human-readable names (Deploy Ninja, Quantum Debugger) appear only in
documentation, not in the YAML frontmatter.
