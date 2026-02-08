---
name: compound
description: Promote valuable knowledge from Flow to Stock — curate learnings from recent work
disable-model-invocation: true
---

Invoke skill `context-persistence`, then execute **Flow → Stock Promotion**:

1. Read `.claude/context/progress.md` (recent work log)
2. For each entry, evaluate: does this contain reusable knowledge?
3. **Present a routing proposal to the human** — do NOT write directly:

```
📋 /compound — Knowledge Promotion Proposal

From progress.md, I found the following promotable learnings:

| # | Learning | Proposed Destination | Reason |
|---|----------|---------------------|--------|
| 1 | "..." | project learnings | Project-specific API detail |
| 2 | "..." | global learnings | Reusable across projects |
| 3 | "..." | code-quality-rules | Universal quality pattern |
| 4 | "..." | discard | Not reusable knowledge |

Adjust any routing? (or "OK" to proceed)
```

4. Wait for human confirmation or adjustments before writing
5. For quality rule candidates, follow the Rule Evolution Protocol in `code-quality-rules`:
   - Propose the rule to the human
   - If approved, add to SKILL.md with examples
6. After confirmation, write to destinations and clean up promoted entries from `progress.md`
7. Report final results

| Destination | Criteria | Example |
|-------------|----------|---------|
| `.claude/context/learnings.md` | Project-specific knowledge | "This API rate-limits at 100req/min" |
| `~/.claude/learnings/global-learnings.md` | Cross-project knowledge | "CORS middleware must come before auth" |
| `code-quality-rules` (self-evolution) | Universal quality rule | "Never use eval()" |
| discard | Not reusable, ephemeral detail | "Fixed typo in line 42" |
