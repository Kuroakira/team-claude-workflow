---
name: compound
description: Promote valuable knowledge from Flow to Stock — curate learnings from recent work
disable-model-invocation: true
---

Invoke skill `context-persistence`, then execute **Flow → Stock Promotion**:

1. Read `.claude/context/progress.md` (recent work log)
2. For each entry, evaluate: does this contain reusable knowledge?
3. Route each learning to the appropriate destination:

| Destination | Criteria | Example |
|-------------|----------|---------|
| `.claude/context/learnings.md` | Project-specific knowledge | "This API rate-limits at 100req/min" |
| `~/.claude/learnings/global-learnings.md` | Cross-project knowledge | "CORS middleware must come before auth" |
| `code-quality-rules` (self-evolution) | Universal quality rule | "Never use eval()" |

4. For quality rule candidates, follow the Rule Evolution Protocol in `code-quality-rules`:
   - Propose the rule to the human
   - If approved, add to SKILL.md with examples
5. After promotion, clean up promoted entries from `progress.md`
6. Report what was promoted and where
