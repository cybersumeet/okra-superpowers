---
name: receiving-code-review
description: >
  Use when you receive code review feedback on your work. Don't use when
  there is no feedback to act on, or when the feedback is already addressed.
  Process feedback systematically to improve code without argument.
---

# Receiving Code Review

Act on review feedback with discipline and without defensiveness.

## Procedure

### 1. Read all feedback first
- Read every comment before acting on any
- Understand the intent, not just the literal suggestion
- Ask for clarification if a comment is unclear

### 2. Categorize responses
- **Accept**: Makes the code better. Implement as suggested or adapt.
- **Discuss**: You disagree or need context. Reply explaining your reasoning.
- **Defer**: Valid point but out of scope. Note for follow-up task.

### 3. Address in batches
- Group related feedback into commits
- Trivial fixes (typos, naming): one batch commit
- Logic changes: separate commit with explanation
- Never mix unrelated feedback in one commit

### 4. Verify after changes
- Re-run tests after every batch
- Re-read the changed code yourself
- Check that you didn't introduce new issues
- Mark comments as resolved only after verification

### 5. Follow up on defers
- Create a new task for deferred feedback
- Link to the original review
- Schedule it so it doesn't disappear

## Anti-patterns

- Arguing with every suggestion
- Marking comments resolved without actually fixing
- Implementing suggestions blindly without understanding
- Leaving "will fix later" without a tracking task

## Output

Addressed feedback with clear commits and no unresolved critical issues.
