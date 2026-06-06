---
name: code-review
description: Comprehensive code review of recent changes with severity-rated findings
trigger: code review, review changes, review diff, check my code
---

# Code Review Skill

Source: AI on Mac Bible, Chapter 8 (Claude Code Mastery) & Chapter 3 (Context Engineering)

## Workflow

1. Run `git diff` (or `git diff --staged` if specified) to see recent changes
2. Identify the language, framework, and conventions from the codebase
3. For each changed file, analyze:
   - **Bugs & Logic Errors** — off-by-ones, null handling, race conditions, incorrect assumptions
   - **Security Issues** — injection, hardcoded secrets, OWASP Top 10, auth bypass
   - **Performance** — unnecessary allocations, N+1 queries, missing indices, blocking calls
   - **Style & Conventions** — consistency with existing codebase patterns
   - **Test Coverage** — do tests cover the changed paths?

## Output Format

Return findings as a markdown table:

| File | Line | Severity | Issue | Suggested Fix |
|------|------|----------|-------|---------------|

Severity levels:
- **Critical** — security vulnerability, data loss, crash in production
- **High** — bug that will hit users, significant performance regression
- **Medium** — code smell, maintainability concern, edge case
- **Low** — style nit, minor improvement opportunity

## Principles

- Don't praise good code. Focus on what could be improved.
- Suggest specific fixes, not general advice.
- Skip style nits unless they hide real bugs.
- Flag any hardcoded credentials, API keys, or secrets as Critical.
- Check for OWASP Top 10 vulnerabilities in web-facing code.
