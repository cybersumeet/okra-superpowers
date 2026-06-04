---
name: subagent-driven-development
description: >
  Use when executing a multi-task plan where each task is substantial enough
  to benefit from a fresh context. Don't use for trivial changes or when
  the tasks are tightly coupled. Each subagent gets isolated context and
  a two-stage review before integration.
---

# Subagent-Driven Development

Execute plans by delegating tasks to subagents with review gates.

## Procedure

### 1. Prepare the task brief
- Extract one task from the plan
- Include full context: relevant code, constraints, design doc
- Define clear acceptance criteria
- Specify output format (file path, code, test results)

### 2. Dispatch the subagent
- Spawn a fresh subagent with only the task context
- No access to unrelated plan tasks
- Set a reasonable timeout

### 3. Stage 1 review: Spec compliance
- Does the output match the task requirements?
- Are the correct files modified?
- Does it follow the project's conventions?
- Reject and retry if not compliant

### 4. Stage 2 review: Code quality
- Readability, naming, comments
- Edge cases and error handling
- Test coverage
- Performance considerations
- Approve or request changes

### 5. Integrate and continue
- Apply approved subagent output to the main branch
- Update the plan progress
- Move to the next task

## Anti-patterns

- Giving subagents the entire plan instead of one task
- Skipping Stage 1 review
- Approving without reading the code
- Not updating the plan after integration

## Output

Task-by-task implementation with quality review at each step.
