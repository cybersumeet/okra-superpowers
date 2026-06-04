---
name: writing-skills
description: >
  Use when creating new skills, editing existing skills, or porting workflows
  into the skill format. Don't use for general documentation — skills are
  specifically for agentic workflows that trigger at runtime.
---

# Writing Skills

Create new agentic skills that can be imported and used by agents.

## Procedure

### 1. Identify the workflow
- What repeatable process does this capture?
- When should it activate? (the description is the routing logic)
- What are the steps, anti-patterns, and outputs?

### 2. Write the SKILL.md

```markdown
---
name: <kebab-case-name>
description: >
  Use when... Don't use when...
  This description is how agents decide to load the skill.
---

# <Title>

## Procedure
### 1. Step one
### 2. Step two
...

## Anti-patterns
- What not to do

## Output
What the skill produces
```

### 3. Add references (optional)
- Create a `references/` folder in the skill directory
- Add examples, templates, or deep-dives
- Agents can load these for additional context

### 4. Test the skill
- Write a test scenario: given X task, does the skill activate?
- Check that the description is clear enough for routing
- Verify the steps are actionable

### 5. Publish
- Save in a git repository
- Paperclip imports from `owner/repo` or full GitHub URLs
- Skills are pinned to the commit at import time

## Skill anatomy

- **Frontmatter**: name, description (routing logic)
- **Body**: detailed instructions, steps, anti-patterns
- **References**: optional supporting files

## Anti-patterns

- Vague descriptions that never trigger or always trigger
- Steps that are too high-level to follow
- No anti-patterns section (missed guardrails)
- Writing skills for one-off tasks

## Output

A complete skill that agents can discover, load, and execute at runtime.
