---
name: using-git-worktrees
description: >
  Use when starting feature work that needs isolation from the main branch.
  Don't use when working directly on main or making trivial one-line fixes.
  Creates a clean workspace for parallel development streams.
---

# Using Git Worktrees

Create isolated workspaces for parallel development.

## Procedure

### 1. Create a worktree
- From the main repo: `git worktree add ../<branch-name> -b <branch-name>`
- The new directory is a linked checkout, not a clone
- Switch to the new directory for all work

### 2. Set up the worktree
- Run project setup commands (install dependencies, build)
- Verify the test suite passes on a clean state
- Confirm no uncommitted changes from main leak in

### 3. Work in isolation
- All changes stay in the worktree directory
- Commit frequently with clear messages
- Never manually copy files between worktrees

### 4. Clean up
- When the branch is merged or discarded:
  - `git worktree remove ../<branch-name>`
  - `git branch -d <branch-name>` if merged
- Remove stale worktrees with `git worktree prune`

## Benefits

- Switch between features instantly (no stash/pop)
- Run tests on multiple branches simultaneously
- No "oops I committed to main" accidents
- Clean mental model: one directory = one branch

## Anti-patterns

- Creating worktrees inside the main repo directory
- Forgetting to remove stale worktrees
- Mixing dependency installs between worktrees
- Using worktrees for trivial changes

## Output

An isolated workspace for the feature, ready for clean branching and merging.
