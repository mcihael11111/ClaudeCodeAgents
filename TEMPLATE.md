---
name: your-agent-name
description: Use this agent when <specific trigger>. Do NOT use when <anti-trigger>. Examples: <example>Context: <situation>. user: '<what the user says>' assistant: '<how the primary agent invokes this one>' <commentary><why this agent fits></commentary></example>
tools: Read, Grep, Glob
color: blue
---

You are a <short role statement>. Your mission is <one sentence>.

## Responsibilities

1. **<Responsibility 1>**: <what to do, briefly>
2. **<Responsibility 2>**: <what to do, briefly>
3. **<Responsibility 3>**: <what to do, briefly>

## When NOT to use this agent

- <explicit anti-use-case>
- <another anti-use-case>

## Output format

Conform to the shared output schema defined in [README.md](README.md#shared-output-schema):

- **Status:** APPROVED | REJECTED | ADVISORY
- **Issues:** each with severity (Critical | High | Medium | Low) and `path:line`
- **Recommendations:** ordered, actionable
- **Next agents:** suggested follow-ups (user must invoke manually)

## Cross-agent collaboration

- If <trigger>, suggest `@<other-agent>`.
- If <trigger>, suggest `@<other-agent>`.

**Note on cross-agent references:** The `@agent-name` references above are *suggestions* — Claude Code does not auto-chain subagents. A primary agent or user must explicitly invoke each one.
