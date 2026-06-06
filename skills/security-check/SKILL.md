---
name: security-check
description: Security audit of recent changes against OWASP Top 10 and credential hygiene
trigger: security check, security review, check for vulnerabilities, audit security
---

# Security Check Skill

Source: AI on Mac Bible, Chapter 13 (Security and Privacy) & Chapter 23 (Threat Modeling)

## Workflow

1. Run `git diff` to identify changed files
2. Scan for credential exposure:
   - Hardcoded API keys, tokens, passwords
   - `.env` files added to version control
   - Private keys or certificates
3. Check OWASP Top 10 for LLM Applications:
   - Prompt injection vulnerabilities
   - Insecure output handling
   - Training data poisoning vectors
   - Denial of service via resource-intensive tool calls
   - Supply chain vulnerabilities (dependencies)
4. Check web application OWASP Top 10:
   - SQL/NoSQL injection
   - XSS (cross-site scripting)
   - Broken authentication
   - Sensitive data exposure
   - Security misconfiguration
5. Check dependency health:
   - Known CVEs in dependencies
   - Outdated packages with security patches available

## Threat Model (from Bible Ch 23)

Realistic threats for AI-enabled applications:
- **Prompt injection** — malicious input that changes model behavior
- **Data leakage** — sensitive data sent to AI vendors unintentionally
- **Credential theft** — API keys, tokens exposed in code or logs
- **Supply chain** — compromised npm/pip packages, model files
- **Insecure deserialization** — untrusted data parsed without validation

## Output Format

```
## Security Audit Results

### Critical Findings
[List with file, line, description, remediation]

### Warnings
[List with file, line, description, recommendation]

### Passed Checks
[Summary of what was checked and passed]

### Recommendations
[General hardening suggestions]
```

## Principles

- Never skip credential scanning — it's the highest-ROI check.
- Flag any secret in version control as Critical, even in test files.
- Check `.gitignore` for missing entries (`.env`, `*.pem`, `credentials.json`).
- Validate that environment variables are used for secrets, not hardcoded values.
- For AI features: check that user input is sanitized before inclusion in prompts.
