---
name: career-artifacts
description: AI-augmented career document generation — applications, cover letters, and job tracking
trigger: job application, cover letter, career document, application materials, apply for job
---

# Career Artifacts Skill

Source: AI on Mac Bible, Chapter 33 (Career Artifacts Applied Playbook) & Chapter 20 (Career Development)

## Workflow

### Per-Application Flow

1. **Receive job description** from user
2. **Receive master resume** (or locate in `resumes/` directory)
3. **Generate tailored materials:**
   - Tailored resume bullet adjustments for top 3 most relevant roles
   - Cover letter draft (250-350 words, no fluff, lead with strongest match)
   - 3 questions to ask the hiring manager
   - Risk assessment: where is the candidate a weaker fit? How to address?
   - Keywords from the JD that should appear in the resume
4. **User reviews and edits** (~15 min)
5. **Log in tracker** (if tracker exists)

### For Resume-Specific Work

Defer to the `resume-tailoring` skill (`skills/resume-tailoring/SKILL.md`) for full resume generation with research, discovery, and multi-format output.

This skill handles lighter-weight application materials and career document management.

## Cover Letter Template

Structure:
1. **Opening** — specific role + company + strongest match point
2. **Body** — 2-3 paragraphs mapping experience to JD requirements
3. **Close** — enthusiasm + availability + call to action

Constraints:
- 250-350 words maximum
- No fluff, no generic statements
- Lead with the single strongest match
- Honest — don't claim experience the user doesn't have
- Match language to job description

## Risk Assessment

For each application, identify:
- Where the candidate is a weaker fit
- How to address each weakness (reframe, acknowledge, mitigate)
- Red flags the hiring manager might see
- Specific JD requirements that aren't well covered

## Application Tracking

If the user maintains a tracker, log:
- Company, role, application date
- Materials submitted (versioned)
- Status: applied → phone screen → onsite → offer → rejected → withdrew
- Notes from each interaction
- Decision (if rejected): why, what to improve

## Principles

- **Truth-preserving**: never claim experience the user doesn't have
- **Quantify**: use numbers wherever possible
- **Match language**: mirror JD terminology (tools, frameworks, methodologies)
- **Lead with relevance**: strongest match first, not chronological
- **Be honest about gaps**: transparent risk assessment builds trust
