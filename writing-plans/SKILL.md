---
name: writing-plans
description: >
  Use when you have an approved design and need to turn it into an actionable
  implementation plan. Don't use when the change is a one-line fix or already
  obvious. Plans should be detailed enough for a junior engineer to execute.
---

# Writing Plans

Convert an approved design into a step-by-step implementation plan.

## Procedure

### 1. Scope the work
- List every file that will be created, modified, or deleted
- Identify dependencies and prerequisites
- Flag risky or uncertain tasks

### 2. Write bite-sized tasks
- Each task should take 2–5 minutes of focused work
- Include the exact file path for every task
- Provide the complete code or diff when the change is mechanical
- Include verification steps: how will you know this task is done correctly?

### 3. Order dependencies
- Sequence tasks so later tasks don't break earlier ones
- Group independent tasks for parallel execution
- Flag tasks that need human approval before continuing

### 4. Write to `.hermes/plans/`
- Save the plan as `plan.md` in the project's `.hermes/plans/` directory
- Plans are living documents — update them if reality changes

## Plan format

```markdown
# Plan: <title>

## Prerequisites
- [ ] branch created
- [ ] tests pass on base branch

## Tasks

### Task 1: <short description>
- File: `path/to/file.ext`
- Action: create / modify / delete
- Code:
  ```<lang>
  <complete code or diff>
  ```
- Verify: <how to confirm this works>

### Task 2: <short description>
...
```

## Anti-patterns

- Vague tasks like "fix the bug" without specifics
- Plans with no verification steps
- Tasks that span multiple unrelated files
- Skipping the plan for "small" changes that later grow

## Output

A saved plan document that a subagent or human can follow task-by-task.
