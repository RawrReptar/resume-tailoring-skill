# CLAUDE.md - Project Instructions

## Available Skills

This repository contains Claude Code skills that should be consulted and used when fulfilling user requests.

### Resume Tailoring Skill

**Location:** `skills/resume-tailoring/SKILL.md`

**When to use:** Any request involving resumes, job applications, career documents, or job search activities. This includes:
- Creating or tailoring a resume for a specific job description
- Batch processing multiple job applications
- Reviewing or improving an existing resume
- Researching companies or roles for job applications
- Discovering and surfacing undocumented work experiences
- Generating cover letters or interview prep materials

**How to use:** Read `skills/resume-tailoring/SKILL.md` for the full workflow. The skill has 5 phases:
1. **Library Build** - Scan existing resumes to build a content library
2. **Research** - Deep company/role research and success profile creation
3. **Template** - Structure and title optimization
4. **Discovery & Assembly** - Surface undocumented experiences, match content with confidence scoring
5. **Generation** - Produce MD, DOCX, and interview prep reports

**Multi-job mode:** For batch processing multiple jobs, also read `multi-job-workflow.md`.

### Supporting References

When executing resume-related tasks, also consult these files for detailed strategies:
- `research-prompts.md` - Templates for JD parsing, company research, and role benchmarking
- `matching-strategies.md` - Content matching algorithms, confidence scoring, and reframing strategies
- `branching-questions.md` - Conversational patterns for experience discovery interviews
- `docs/schemas/batch-state-schema.md` - Data structures for multi-job batch processing
- `docs/schemas/job-schema.md` - Job object lifecycle and schema

## Core Principles

When working on any task in this repo, follow these principles from the skill's design philosophy:

- **Truth-Preserving Optimization:** NEVER fabricate experience. Intelligently reframe and emphasize real experiences. Be transparent about gaps.
- **Holistic Person Focus:** Surface undocumented experiences. Value volunteer work, side projects, and diverse backgrounds.
- **User Control:** Provide checkpoints at key decisions. Present options, not mandates. Allow adjustments.
