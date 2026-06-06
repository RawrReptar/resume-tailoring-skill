# CLAUDE.md - Project Instructions

## Skills Index

Before fulfilling any user request, scan this index to identify which skill(s) apply. Read the matching SKILL.md file(s) before proceeding. Multiple skills can be combined for complex requests.

### Quick Lookup Table

| Keyword / Intent | Skill | Location |
|---|---|---|
| resume, tailor, job description, JD | Resume Tailoring | `skills/resume-tailoring/SKILL.md` |
| batch, multiple jobs, multi-job | Resume Tailoring (multi-job) | `multi-job-workflow.md` |
| cover letter, application materials | Career Artifacts | `skills/career-artifacts/SKILL.md` |
| interview, mock interview, STAR | Interview Prep | `skills/interview-prep/SKILL.md` |
| code review, review diff, check code | Code Review | `skills/code-review/SKILL.md` |
| security, vulnerability, credentials | Security Check | `skills/security-check/SKILL.md` |
| prompt, context engineering, improve prompt | Context Engineering | `skills/context-engineering/SKILL.md` |

### Skill Details

#### 1. Resume Tailoring
**Location:** `skills/resume-tailoring/SKILL.md`
**Triggers:** resume, tailor, job description, JD, career document, job application, apply
**Use when:** Creating or tailoring resumes for specific job descriptions, batch processing multiple applications, reviewing/improving existing resumes, researching companies/roles, discovering undocumented experiences.
**Phases:** Library Build → Research → Template → Discovery & Assembly → Generation
**Multi-job mode:** Read `multi-job-workflow.md` for batch processing 3-5 similar jobs.
**Supporting files:**
- `research-prompts.md` — JD parsing, company research, role benchmarking templates
- `matching-strategies.md` — Content matching algorithms, confidence scoring, reframing
- `branching-questions.md` — Conversational patterns for experience discovery
- `docs/schemas/batch-state-schema.md` — Batch processing data structures
- `docs/schemas/job-schema.md` — Job object lifecycle and schema

#### 2. Career Artifacts
**Location:** `skills/career-artifacts/SKILL.md`
**Triggers:** cover letter, application materials, job application workflow, career documents, job tracker
**Use when:** Generating cover letters, application materials, risk assessments, or managing application tracking. For full resume generation, defer to Resume Tailoring skill.

#### 3. Interview Prep
**Location:** `skills/interview-prep/SKILL.md`
**Triggers:** interview prep, mock interview, interview questions, STAR stories, company research for interview
**Use when:** Preparing for interviews — company research packages, likely questions, STAR story mapping, mock interview practice, post-interview reflection.

#### 4. Code Review
**Location:** `skills/code-review/SKILL.md`
**Triggers:** code review, review changes, review diff, check my code, review PR
**Use when:** Reviewing code changes for bugs, security issues, performance problems, and style consistency. Outputs severity-rated findings table.

#### 5. Security Check
**Location:** `skills/security-check/SKILL.md`
**Triggers:** security check, security review, vulnerability scan, credential check, audit
**Use when:** Auditing code for security vulnerabilities — OWASP Top 10, credential exposure, dependency CVEs, prompt injection risks.

#### 6. Context Engineering
**Location:** `skills/context-engineering/SKILL.md`
**Triggers:** improve prompt, better prompt, context engineering, optimize prompt, prompt design
**Use when:** Designing or improving prompts, structuring context for AI tasks, diagnosing context failures (burst, poisoning, noise, conflict).

## Reference Documentation

- `docs/reference/ai-on-mac-bible-v4.md` — Comprehensive AI on Mac reference (33 chapters). Consult for deep dives on: hardware optimization (Ch 1), cost economics (Ch 2), context engineering (Ch 3), local inference (Ch 4), security (Ch 13), MCP ecosystem (Ch 15), career development (Ch 20).

## Core Principles

All skills follow these principles:

- **Truth-Preserving Optimization:** NEVER fabricate experience. Intelligently reframe and emphasize real experiences. Be transparent about gaps.
- **Holistic Person Focus:** Surface undocumented experiences. Value volunteer work, side projects, and diverse backgrounds.
- **User Control:** Provide checkpoints at key decisions. Present options, not mandates. Allow adjustments.
- **Specificity Over Vagueness:** Concrete targets, not abstract advice. Show, don't tell.
- **Security First:** Never commit secrets. Validate at system boundaries. Check OWASP Top 10.
