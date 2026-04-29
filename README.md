# AIX Knowledge Vault

> AI Exploration Center, SUNY Polytechnic Institute  
> Shared knowledge repository — team-facing, AI-assisted, human-reviewed

---

## What this is

This is the shared knowledge base for the AIX Center and its collaborators. Notes are a mix of human-authored and AI-generated content. All AI-generated notes enter as `review_status: unreviewed`.

This vault is not a filing system. It's a **trail network**. Add folders when work accumulates. Link aggressively. Close paths when threads end. The structure will emerge from the work.

---

## How it's organized

**Folders are hubs.** Any folder is a hub. Add one when a body of work needs a home — not before. Obsidian reads the whole tree, so everything is findable regardless of where it lives.

**`_inbox/`** is the only required folder. Unplaced, unreviewed, or just-generated notes go here. Triage periodically.

**Everything else is emergent.** Current hubs reflect work in progress, not a permanent org chart:

```
_inbox/          ← everything lands here first

ai-education/    ← curriculum, pedagogy, course development
                    ai-rtw, dwit, sts190, nyhmma, gaming (Nick Lejeune)

ai-analysis/     ← research, policy, applied analytical work
                    herkimer, dac/tdac, m-dun

ai-platform/     ← infrastructure, tools, knowledge architecture
                    workbench, zettel, obsidian-vault, agentic (Alvin, Asela)

ai-africa/       ← Nigeria + Cameroon partnerships; COIL
                    noun/nuc, fut-minna, u-buea, u-yaounde
                    (cross-cuts everything; lives at top level for now)

_people/         ← one note per person; linked from everywhere else
```

If your work doesn't fit, **make a folder**. Leave a note in `_inbox/` pointing to it so others can find it.

---

## Note conventions

Minimum frontmatter for any note:

```yaml
---
title: 
date: 
status: draft | active | archived
review_status: unreviewed | reviewed
generated_by: human | claude | chatgpt | mixed
projects:
  - "[[project-name]]"
people:
  - "[[Name]]"
tags:
  - 
---
```

Use wikilink values for `projects` and `people` so the graph stays connected:
```yaml
projects:
  - "[[ai-rtw]]"
people:
  - "[[Nick Lejeune]]"
```

---

## Trail-closing convention

When a thread ends — project done, path abandoned, question answered — add to the note:

```yaml
status: archived
closed: 2026-04-29
closed_note: "Leads to [[wherever it went]]"
```

Don't delete. Leave the trail.

---

## What goes here vs. your personal vault

Personal thinking, raw drafts, and private analysis live in your local vault. When something matures and belongs to the team, move or copy it here. That threshold is also a review step.

---

*Structure is a hypothesis. Folders are cheap. Links are the real architecture.*

*Last updated: 2026-04-29*
