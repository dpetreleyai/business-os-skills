---
name: sop-writer
description: >
  Turn a described process into a numbered, delegable SOP document. Use when
  the owner says "write an SOP", "document how we do X", "make a checklist
  for", or describes a recurring process that lives only in someone's head.
---

# SOP Writer

Turn tribal knowledge into a document someone new could follow on day one.

## Procedure

1. **Listen.** Let the owner describe the process. Ask only for gaps a new
   hire would trip on: trigger ("when does this start?"), inputs, tools/logins
   involved, the decision points, what "done" looks like, who owns it.
2. **Draft** using this shape:
   - Title, owner, trigger, frequency
   - Tools needed (named, with where to find access — never the credentials)
   - Numbered steps, one action each; decision points as "If X → step N"
   - Definition of done + where the output goes
   - Common mistakes (ask for one or two)
3. **Save** to `<department>/output/<verb>-<object>-sop-v1.md` (naming per
   `_shared/naming-conventions.md`). Pick the department from the router; ask
   only if genuinely ambiguous.
4. **Wire it in**: add a line to the department's `CONTEXT.md` under
   "Recurring workflows" pointing at the SOP, and mention it in the vault
   department note if one exists.
5. Read the finished SOP back in three sentences and ask what's wrong with it.
   Fix, bump to `-final` when approved.

## Rules

- One process per document. A "process" that needs three documents is three
  processes — say so.
- Write for the least-context reader: no internal shorthand without a gloss.
- Never invent steps: unknowns become `# REFINE: <question>` lines.
