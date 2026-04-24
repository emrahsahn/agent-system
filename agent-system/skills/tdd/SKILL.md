---
name: tdd
description: Use when implementing features, fixing bugs, or refactoring. Enforces RED-GREEN-REFACTOR and test-first execution.
---

# TDD - Test-Driven Development

## Objective

Build reliable changes with test-first delivery and explicit regression protection.

## Steps

1. RED
   - Write a failing test that captures intended behavior.
   - Confirm the failure is meaningful.

2. GREEN
   - Implement the minimum code to pass the test.
   - Avoid extra scope until all target tests pass.

3. REFACTOR
   - Improve design and readability without changing behavior.
   - Keep tests green after each refactor step.

## Coverage targets

- General logic: at least 80 percent
- Critical flows (auth, billing, security): target full path coverage

## Output

- Added/updated test list
- Pass/fail summary
- Refactor notes
- Remaining technical risks
