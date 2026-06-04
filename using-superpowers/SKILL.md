---
name: using-superpowers
description: >
  Use when starting any coding session to understand what skills are available
  and how they compose. Don't use when you already know which skill applies.
  This is the entry-point skill that introduces the agentic methodology.
---

# Using Superpowers

You have access to a library of composable development methodology skills.
Each skill is a structured workflow that activates when relevant.

## How skills work

1. **Discovery**: The system presents skill descriptions at runtime
2. **Routing**: The agent reads the description to decide if the skill applies
3. **Loading**: If relevant, the full SKILL.md content is injected into context
4. **Execution**: The agent follows the instructions in the skill

## Skill categories

| Category | Skills |
|----------|--------|
| **Process** | brainstorming, writing-plans, executing-plans, dispatching-parallel-agents |
| **Implementation** | test-driven-development, subagent-driven-development, using-git-worktrees |
| **Review** | requesting-code-review, receiving-code-review, verification-before-completion |
| **Debugging** | systematic-debugging |
| **Completion** | finishing-a-development-branch |
| **Meta** | writing-skills, using-superpowers |

## Workflow order

For a typical feature:

1. **brainstorming** → clarify and design
2. **using-git-worktrees** → create isolated workspace
3. **writing-plans** → break into tasks
4. **test-driven-development** → RED-GREEN-REFACTOR for each task
5. **subagent-driven-development** or **executing-plans** → implement
6. **requesting-code-review** → self-review between tasks
7. **verification-before-completion** → confirm it works
8. **finishing-a-development-branch** → merge or PR

## Rules

- Check for relevant skills before any task
- Skills are mandatory workflows, not suggestions
- Multiple skills can be active simultaneously
- If no skill matches, use your best judgment

## Output

Awareness of available skills and the discipline to use them.
