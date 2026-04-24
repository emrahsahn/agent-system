---
name: code-review
description: Use after code changes and before merge. Performs structured review for quality, correctness, security, and maintainability.
---

# Code Review

## Objective

Identify and prioritize issues before release with actionable fix guidance.

## Steps

1. Inspect change scope
   - Understand feature intent, touched files, and risk areas.

2. Review quality and correctness
   - Readability, modularity, and consistency
   - Edge cases, error handling, async behavior

3. Review performance and security
   - Performance bottlenecks and unnecessary work
   - Input validation, auth checks, sensitive data handling

4. Review test adequacy
   - Coverage for new behavior
   - Negative and failure-path scenarios

## Severity model

- Critical: must fix before merge
- High: fix in short term
- Medium: planned backlog
- Low: improvement opportunity

## Output

- Findings grouped by severity
- For each finding include:
  - file
  - issue
  - impact
  - recommended fix
