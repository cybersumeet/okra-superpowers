---
name: finishing-a-development-branch
description: >
  Use when implementation is complete, all tests pass, and you are ready to
  close out a feature branch. Don't use when there are failing tests or
  uncommitted work. Presents merge/PR/cleanup options cleanly.
---

# Finishing a Development Branch

Cleanly close out a completed feature branch.

## Procedure

### 1. Final verification
- Run the full test suite one last time
- Run linting and type checks
- Review the full diff since branch creation
- Ensure no debug code, TODOs, or secrets remain

### 2. Present options
Offer the user 4 options:

1. **Merge to main** — Fast-forward or merge commit if allowed
2. **Open a PR** — Push branch, create PR with summary
3. **Keep the branch** — Leave as-is for now
4. **Discard** — Abandon changes with confirmation

### 3. Execute chosen option
- **Merge**: `git checkout main && git merge <branch> && git push`
- **PR**: `git push -u origin <branch>`, generate PR description
- **Keep**: Document why it's being kept
- **Discard**: `git branch -D <branch>` and remove worktree

### 4. Clean up
- Remove the worktree if one was used
- Delete remote branch after merge
- Update any related issues or project boards
- Present a summary of what was accomplished

## PR description template

```markdown
## Summary
<one-line description>

## Changes
- <bullet list of key changes>

## Testing
- <how this was tested>

## Notes
- <anything reviewers should know>
```

## Anti-patterns

- Merging with failing tests
- Leaving stale branches on remote
- Not summarizing what the branch accomplished
- Deleting without confirming the user wants to discard

## Output

A cleanly closed branch, merged or preserved as requested.
