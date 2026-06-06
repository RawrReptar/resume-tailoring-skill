---
name: context-engineering
description: Design optimal prompts and context for AI tasks using the Karpathy mental model
trigger: improve prompt, context engineering, better prompt, optimize prompt, design prompt
---

# Context Engineering Skill

Source: AI on Mac Bible, Chapter 3 (Context Engineering)

## Mental Model

Think of the LLM as a CPU, the context window as RAM. Your job is the operating system — deciding what data and code goes into RAM at any given moment. (Karpathy analogy)

## The Six-Part Prompt Template

```
[ROLE]        — Who is the model in this conversation?
[CONTEXT]     — What background does it need?
[TASK]        — What is the specific job?
[FORMAT]      — What should the output look like?
[CONSTRAINTS] — Limits, style requirements, do-nots
[EXAMPLES]    — Demonstrations of desired output
```

Not every prompt needs all six. Short tasks: TASK + INPUT. Complex tasks: full structure.

## Three Layers of Context

1. **Instructions** — what the model should do (system prompts, few-shot examples, rules)
2. **Knowledge** — what the model needs to know (documents, retrieved chunks, history)
3. **Tools** — what the model can do (function definitions, MCP servers, capabilities)

Balance all three. Heavy instructions + light tools = knows what to do but can't act. Heavy knowledge + light instructions = has facts but no direction.

## Failure Modes to Diagnose

- **Context burst** — window fills up, model loses track of earlier instructions
- **Context poisoning** — retrieved content contains errors that propagate
- **Context noise** — too much irrelevant material drowns signal
- **Context conflict** — different sources tell contradictory things

## Workflow

When asked to improve a prompt or design context:

1. **Identify the task type**: classification, generation, extraction, analysis, conversation
2. **Assess current failure mode**: which of the four failures is occurring?
3. **Apply the six-part template** to structure the prompt
4. **Add examples**: show, don't tell — 3-5 examples covering edge cases
5. **Be specific over vague**: define concrete targets (word count, format, style reference)
6. **Use effective negatives**: reference specific tokens/formats to avoid, not vague instructions
7. **Consider caching**: repeated context should use prompt caching
8. **Test and iterate**: evaluate output quality, adjust context balance

## Key Principles

- **Show, don't tell.** Few-shot examples beat extensive explanation.
- **Specificity over vagueness.** "Under 150 words, confident tone, no corporate-speak" beats "make it better."
- **Negative instructions work** when they reference specific tokens or formats to avoid.
- **Negative instructions fail** when vague: "don't be too long" or "don't sound like AI."
- **The harness matters.** Context engineering is what the model sees. Harness engineering (CLAUDE.md, hooks, permissions) is what it can do. You need both.
