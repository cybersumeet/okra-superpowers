---
name: requesting-code-review
description: >
  Use between implementation tasks or before finishing a branch. Don't use
  when the change is trivial or when working alone without review process.
  Reviews catch deviation from plan and quality issues before they compound.
---

# Requesting Code Review

Review your own work against the plan and quality standards.

## Procedure

### 1. Review against the plan
- Does the code implement what the task specified?
- Are all files from the plan modified as expected?
- Is anything missing or extra?

### 2. Severity classification
- **Critical**: Wrong behavior, security issue, broken tests. Blocks progress.
- **Warning**: Code smell, missing edge case, unclear naming. Should fix.
- **Info**: Suggestion, style preference, future consideration. Optional.

### 3. Report findings
- List issues by severity
- For critical issues: stop and fix before continuing
- For warnings: note and fix if quick, else add to plan
- For info: note for future reference

### 4. Pre-commit checklist
- Tests pass
- Linting passes
- No debug code left in
- Commit messages are clear
- No secrets or credentials in diff

## Anti-patterns

- Skipping review because "it's just a small change"
- Only reviewing after everything is done
- Ignoring critical issues to meet a deadline
- Not documenting why a warning was accepted

## Output

A review report with classified issues and a decision: continue, fix, or
escalate.
