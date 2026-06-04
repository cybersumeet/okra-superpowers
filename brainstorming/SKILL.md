---
name: brainstorming
description: >
  Use when starting any new feature, project, or significant change. Don't use
  when fixing a typo, applying a trivial config change, or extending existing
  code in an obvious way. This skill forces structured design thinking before
  implementation to prevent expensive rework.
---

# Brainstorming

Before writing any code, understand the real problem. This skill activates at
the start of any non-trivial engineering task.

## Procedure

### 1. Clarify the request
- Ask clarifying questions until the goal is unambiguous
- Identify the user, the pain point, and the success metric
- Distinguish between "must have" and "nice to have"
- Check for unstated assumptions

### 2. Explore alternatives
- Propose at least 2 distinct approaches
- List tradeoffs (complexity, maintenance, performance, scope)
- Reference existing patterns in the codebase
- Consider what you would regret 6 months from now

### 3. Present in chunks
- Break the design into 2–5 sections
- Each section must be short enough to read in one screen
- Numbered options where the user must choose
- Never present a wall of text; pause for feedback

### 4. Save the design
- Write the agreed design to a `.design.md` or design document
- Include the decisions, rejected alternatives, and why
- The design document becomes the spec for the implementation plan

## Anti-patterns

- Jumping straight to code
- Asking "what tech stack?" before "what problem?"
- Presenting a single option
- Over-engineering before understanding constraints

## Output

A saved design document that another engineer could implement without asking
further questions.
