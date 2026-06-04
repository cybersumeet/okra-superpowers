---
name: executing-plans
description: >
  Use when you have a written plan and need to implement it. Don't use when
  there is no plan — write one first. Execute tasks in order, verify each
  checkpoint, and pause for human review at designated gates.
---

# Executing Plans

Execute a written plan with discipline and checkpoints.

## Procedure

### 1. Read the plan
- Load the full plan from `.hermes/plans/plan.md`
- Confirm prerequisites are met
- Understand the full scope before starting

### 2. Execute one task at a time
- Follow the exact file paths and code from the plan
- Do not improvise beyond the plan unless you find a blocker
- Run verification steps after every task

### 3. Checkpoint reviews
- After every N tasks (or at designated gates), report status
- Report: completed tasks, any deviations, next tasks, blockers
- Wait for human approval before continuing past a checkpoint gate

### 4. Handle deviations
- If a task is impossible as written, stop and report
- Propose an updated plan rather than improvising
- Never silently change the plan

### 5. Complete and verify
- Run the full test suite after all tasks
- Verify the original design goals are met
- Present a summary of changes

## Anti-patterns

- Starting without reading the whole plan
- Combining multiple planned tasks into one giant change
- Changing the plan without updating the document
- Skipping verification because "it looks right"

## Output

Implemented code that matches the approved plan, with a final verification
report.
