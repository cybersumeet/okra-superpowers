---
name: systematic-debugging
description: >
  Use when encountering any bug, test failure, or unexpected behavior. Don't
  use when the fix is already obvious. Follows a 4-phase root cause process
  to avoid guessing and spraying fixes.
---

# Systematic Debugging

Find root causes methodically instead of guessing.

## Procedure

### Phase 1: Understand
- Read the error message carefully. What exactly failed?
- Identify the failing line or component
- Reproduce the issue consistently
- Note the environment: OS, versions, recent changes

### Phase 2: Isolate
- Narrow down the scope of the problem
- Use binary search: comment out half the code, test, repeat
- Check the last known good commit
- Create a minimal reproduction case

### Phase 3: Hypothesize
- Form a specific theory about the root cause
- The theory must be falsifiable: "If X is true, then Y will happen"
- List at least 2 alternative theories
- Prioritize theories by likelihood and testability

### Phase 4: Test and Fix
- Design an experiment to confirm or reject the leading theory
- Run the experiment
- If confirmed: fix the root cause, not the symptom
- If rejected: move to the next theory
- Verify the fix and check for regressions

## Techniques

- **Root cause tracing**: Follow the error backward through the call stack
- **Defense in depth**: Check assumptions at every layer
- **Condition-based waiting**: When timing matters, add explicit waits/retries

## Anti-patterns

- Changing code randomly until it works
- Fixing the symptom without understanding the cause
- Not reproducing before fixing
- Skipping regression testing after a fix
- Assuming the bug is in someone else's code

## Output

A root cause explanation and a verified fix with no regressions.
