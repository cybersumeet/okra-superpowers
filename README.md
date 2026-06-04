# Okra Superpowers

Agentic skills framework for [Paperclip AI](https://paperclip.inc). A set of composable development methodology skills that agents load at runtime to follow structured workflows.

## Skills

| Category | Skill | Description |
|----------|-------|-------------|
| **Process** | [brainstorming](brainstorming/SKILL.md) | Structured design thinking before implementation |
| | [writing-plans](writing-plans/SKILL.md) | Convert designs into actionable implementation plans |
| | [executing-plans](executing-plans/SKILL.md) | Execute written plans with checkpoints |
| | [dispatching-parallel-agents](dispatching-parallel-agents/SKILL.md) | Run independent tasks concurrently |
| **Implementation** | [test-driven-development](test-driven-development/SKILL.md) | RED-GREEN-REFACTOR discipline |
| | [subagent-driven-development](subagent-driven-development/SKILL.md) | Delegate tasks to subagents with review |
| | [using-git-worktrees](using-git-worktrees/SKILL.md) | Isolated workspaces for parallel branches |
| **Review** | [requesting-code-review](requesting-code-review/SKILL.md) | Self-review against plan and standards |
| | [receiving-code-review](receiving-code-review/SKILL.md) | Act on feedback systematically |
| | [verification-before-completion](verification-before-completion/SKILL.md) | Confirm fixes before moving on |
| **Debugging** | [systematic-debugging](systematic-debugging/SKILL.md) | 4-phase root cause process |
| **Completion** | [finishing-a-development-branch](finishing-a-development-branch/SKILL.md) | Merge/PR/cleanup workflow |
| **Meta** | [using-superpowers](using-superpowers/SKILL.md) | Entry point — how skills compose |
| | [writing-skills](writing-skills/SKILL.md) | Create new skills following best practices |

## Import into Paperclip

### Via UI
Paste this URL into the **Skills** page source field:

```
https://github.com/cybersumeet/okra-superpowers
```

Or import a single skill:

```
https://github.com/cybersumeet/okra-superpowers/tree/main/brainstorming
```

### Via API

```bash
curl -X POST "$PAPERCLIP_API_URL/api/companies/$COMPANY_ID/skills/import" \
  -H "Authorization: Bearer $PAPERCLIP_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{ "source": "https://github.com/cybersumeet/okra-superpowers" }'
```

### Assign to agents

```bash
curl -X POST "$PAPERCLIP_API_URL/api/agents/$AGENT_ID/skills/sync" \
  -H "Authorization: Bearer $PAPERCLIP_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "desiredSkills": [
      "paperclip",
      "brainstorming",
      "writing-plans",
      "test-driven-development",
      "systematic-debugging"
    ]
  }'
```

## Skill format

Each skill is a folder containing a `SKILL.md` with YAML frontmatter:

```yaml
---
name: skill-name
description: >
  Use when... Don't use when...
---
```

The `description` is routing logic — agents read it to decide whether to load
the full skill body at runtime.

## License

MIT
