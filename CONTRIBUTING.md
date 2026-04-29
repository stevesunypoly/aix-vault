# Contributing to the AIX Vault

Welcome. This vault is a shared knowledge base, not a shared document. The social contract is light but important.

---

## The one rule

**Don't overwrite someone else's note.** If you disagree, add a note and link to it. If something is wrong, add a `see-also` or a new note with your correction. Leave trails, don't erase them.

---

## How to add

1. Drop new notes in `_inbox/` first if you're unsure where they belong
2. Add a folder (hub) if your work needs a home — no permission needed
3. Link liberally — wikilinks are how the vault thinks
4. Fill out frontmatter, minimum: `title`, `date`, `status`, `generated_by`

---

## How to edit

- Your own notes: edit freely
- Someone else's note: add a comment block at the bottom, or create a response note and link back
- AI-generated notes: flip `review_status` to `reviewed` once you've read and verified

---

## Git hygiene

- Pull before you push
- Small commits, one topic at a time
- Commit message = what you added, not "update notes"
- If you get a merge conflict on a `.md` file, don't panic — they're text, conflicts are readable

---

## The first project

**How to build the AIX knowledge base** — this is the seed question the vault exists to answer. Start there. Add notes, links, questions, half-ideas. The vault is the answer and the process simultaneously.

Specific thread to explore: can we put a TiddlyWiki query layer (Node.js) on top of this vault and expose it to Claude via MCP? See `ai-platform/tw-obsidian-mcp-stub.md`.

---

## People

| Name | Role | Focus |
|---|---|---|
| Steve | Co-Director AIX | Framework, direction |
| Alvin | Agentic AI lead | Automation, pipeline, delegation infrastructure |
| Ayush | AIX team | TW/Obsidian/MCP exploration |
| Asela | AIX team | Agentic AI, DAC-AC |
| Paul | AIX team | Wikipedia/Wikiversity, OER |

---

*The vault is the lab. Build in public.*
