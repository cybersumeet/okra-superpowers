---
name: verification-before-completion
description: >
  Use before claiming any work is done, fixed, or passing. Don't use when the
  verification is already built into the workflow (e.g., CI already ran).
  Catch false positives: things that look fixed but aren't.
---

# Verification Before Completion

Ensure a fix actually works before moving on.

## Procedure

### 1. Reproduce the original issue
- Re-run the exact steps that triggered the bug
- Confirm the bug existed in the first place
- Note the exact error message or behavior

### 2. Apply the fix
- Make the minimal change that addresses the root cause

### 3. Verify the fix
- Re-run the exact same reproduction steps
- Confirm the issue no longer occurs
- Check edge cases that could break with the fix

### 4. Verify nothing else broke
- Run the full relevant test suite
- Run integration tests if available
- Check for regressions in related functionality

### 5. Document
- Note what was broken and how it was fixed
- Include the reproduction steps in the commit message or PR
- If tests were added, reference them

## Anti-patterns

- "It should work now" without testing
- Only testing the happy path
- Assuming the fix is correct because the code looks right
- Moving on because CI is slow

## Output

Confirmed fix with reproduction steps, test results, and no regressions.
