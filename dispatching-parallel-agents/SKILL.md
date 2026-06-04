---
name: dispatching-parallel-agents
description: >
  Use when you have 2 or more independent tasks that can be worked on
  concurrently without blocking each other. Don't use when tasks have
  dependencies — sequence those instead. Useful for research, code review,
  testing, or multi-file refactors.
---

# Dispatching Parallel Agents

Run independent tasks concurrently using subagents.

## Procedure

### 1. Decompose the work
- Identify tasks with no shared files or dependencies
- Each task must be self-contained with its own context
- Define clear inputs and expected outputs for each

### 2. Prepare contexts
- For each subagent, provide:
  - The exact task description
  - Relevant file paths and code snippets
  - Constraints and boundaries
  - Expected deliverable format

### 3. Dispatch concurrently
- Launch all subagents simultaneously
- Each works in an isolated context
- Set a timeout or checkpoint for long-running tasks

### 4. Collect and integrate
- Gather results from all subagents
- Resolve any conflicts between parallel outputs
- Integrate into the main branch or plan
- Verify integration tests pass

## Limits

- Maximum 3 concurrent subagents per dispatch (configurable)
- Each subagent has no memory of the others
- Shared state must be passed explicitly

## Anti-patterns

- Dispatching interdependent tasks in parallel
- Not providing enough context for standalone work
- Launching subagents for trivial 1-minute tasks
- Ignoring conflicts between parallel outputs

## Output

Merged results from all subagents, integrated and verified.
