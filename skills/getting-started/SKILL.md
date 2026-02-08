---
name: getting-started
description: Use when starting a new session, resuming after compact/clear, or beginning a new implementation task.
---

# Claude Praxis

AI as a mirror — articulate "why" at every step, accumulate knowledge across projects.

## Core Philosophy

1. **Understand, not just build** - Every phase forces you to articulate WHY: why this design, why this approach, why not alternatives
2. **You own it** - AI implements and ensures quality. But the deliverables are yours to explain. "AI said so" is not an answer
3. **Compound growth** - Knowledge from each project accumulates as learnings, making the next project's decisions sharper
4. **Self-evolving rules** - Quality standards grow from real experience, captured as explicit rules

## Skills

| Skill | When to Use |
|-------|-------------|
| `code-quality-rules` | Always during implementation. Enforces and evolves quality rules. |
| `systematic-debugging` | When investigating bugs, errors, or unexpected behavior. 4-phase root cause analysis. |
| `context-persistence` | When preserving state across compact/clear. Write auto, read manual. |
| `design-doc-format` | When creating Design Docs. Notion-compatible format. |
| `incremental-review` | During implementation. Show small changes with reasoning. |

## Core Workflow

```
┌─────────────────────────────────────────────────────┐
│ 1. Research Phase (/research)                       │
│    - Understand the problem space and prior art     │
│    - Ask "why" before deciding "what"               │
└─────────────────────────────────────────────────────┘
                        ↓
┌─────────────────────────────────────────────────────┐
│ 2. Design Phase (/design)                           │
│    - Articulate your design rationale               │
│    - Document alternatives and WHY you chose this   │
│    - Submit for review                              │
└─────────────────────────────────────────────────────┘
                        ↓
┌─────────────────────────────────────────────────────┐
│ 3. Planning Phase (/plan)                           │
│    - Break into steps you can explain               │
│    - Each step has a clear purpose                  │
└─────────────────────────────────────────────────────┘
                        ↓
┌─────────────────────────────────────────────────────┐
│ 4. Implementation Phase (/implement)                │
│    - Build with TDD and quality rules               │
│    - Issue found → understand why → update rules    │
└─────────────────────────────────────────────────────┘
                        ↓
┌─────────────────────────────────────────────────────┐
│ 5. Compound Phase (/compound)                       │
│    - Extract what you learned                       │
│    - Carry it forward to the next project           │
└─────────────────────────────────────────────────────┘
```

## Feedback Loop During Implementation

```
Issue found ──→ Discuss with human ──→ Decide direction
    ↓                                      ↓
    └──────────────────────────────────────┤
                                           ↓
                                   Update Doc first
                                           ↓
                                   Re-implement
                                           ↓
                                   Propose rule addition?
                                       ↓      ↓
                                      Yes     No
                                       ↓      ↓
                                 Update SKILL.md  Move on
```

## How to Use Skills

**If a skill exists for the task, you must use it.**

1. Receive a task
2. Check if a relevant skill exists
3. If yes, **always** follow that skill
4. If the skill doesn't cover something, consult the human

## Session Start Checklist

When starting a new session:

1. **Check current state**
   - Any tasks in progress?
   - Does a Design Doc exist?
   - Which Phase is complete?

2. **Restore context**
   - Read necessary documents
   - Identify previous interruption point

3. **Review quality rules**
   - Read the `code-quality-rules` skill
   - Check project-specific rules

## Recovery from compact/clear

When context is lost, check persistence files first:

```
1. Check if .claude/context/ files exist (SessionStart notifies this)
2. If task_plan.md exists → read it for current task state
3. If progress.md exists → read recent entries for context
4. If neither exists → ask the human for file paths
5. Read the Design Doc and implementation plan
6. Resume from the identified point
```
