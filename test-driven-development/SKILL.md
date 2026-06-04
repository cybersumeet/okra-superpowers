---
name: test-driven-development
description: >
  Use when implementing any feature or bugfix that involves code changes.
  Don't use when the task is purely documentation, configuration, or
  infrastructure without logic to test. Enforces RED-GREEN-REFACTOR discipline.
---

# Test-Driven Development

Write tests before code. Every code change must be driven by a failing test.

## Procedure

### 1. RED — Write a failing test
- Describe the behavior you want in a test
- Run the test and watch it fail
- The failure must be for the right reason (not a syntax error)
- Commit the failing test

### 2. GREEN — Write minimal code
- Write the simplest code that makes the test pass
- No refactoring, no edge cases, no "while I'm here"
- Run the test and watch it pass
- Commit the passing code

### 3. REFACTOR — Clean up
- Improve the code while keeping all tests green
- Extract helpers, rename variables, remove duplication
- Run the full test suite after each refactor
- Commit the refactored code

### 4. Delete code written before tests
- If you wrote implementation code before tests, delete it
- Start over with RED-GREEN-REFACTOR
- No exceptions

## Rules

- A passing test without a prior failing test is suspicious
- Never commit with failing tests (except the intentional RED commit)
- Tests are documentation — name them clearly
- Test behavior, not implementation

## Anti-patterns

- Writing all tests, then all code
- Testing private methods directly
- Mocking everything
- Ignoring flaky tests
- Writing tests after the fact to "cover" code

## Output

Working code with a suite of tests that document and verify behavior.
