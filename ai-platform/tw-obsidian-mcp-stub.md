---
title: TiddlyWiki Query Layer on Obsidian Vault via MCP
date: 2026-04-29
status: stub
review_status: unreviewed
generated_by: claude
people:
  - "[[Alvin]]"
  - "[[Ayush]]"
  - "[[Paul]]"
projects:
  - "[[ai-platform]]"
  - "[[zettelkasten]]"
tags:
  - tiddlywiki
  - obsidian
  - mcp
  - node
  - agentic
  - vault-infrastructure
---

## The idea

TiddlyWiki's Node.js edition can run headlessly as a query engine. An Obsidian vault is just a folder of `.md` files with YAML frontmatter. If we map Obsidian notes → TiddlyWiki tiddlers (YAML fields → TW fields, body → `text` field), we get TW's full filter/transclusion syntax operating on vault content.

Expose that via an MCP server and Claude can query the vault like this:

```
get_field("suny-poly", "formal-name")
→ "SUNY Polytechnic Institute"

query("[tag[institution]get[formal-name]]")
→ ["SUNY Polytechnic Institute", "FUT Minna", ...]
```

## Why it matters

- TiddlyWiki field transclusion is more powerful than Dataviewjs for inline queries
- MCP gives Claude live read/write access to the vault
- The vault becomes queryable *and* writable from a Claude session
- This is the AIXZ goal from a different angle — corpus queryable by Claude with TW's expressive power

## What needs building

1. **Obsidian → TW converter** — parse `.md` + YAML → tiddler objects (~100 lines Python or Node)
2. **TW Node.js headless instance** — load converted tiddlers, expose filter API
3. **MCP server wrapper** — tools: `get_field`, `query`, `transclude`, `write_note`
4. **Write-back** — MCP tool that writes results back as `.md` files to the vault

## Open questions

- How do we handle Obsidian wikilinks `[[note]]` vs TW transclusion `{{note}}`?
- Do we convert on the fly or maintain a parallel TW store?
- Read-only first, or write from the start?
- Which vault subset do we build against first — `ai-platform/` itself?

## First step

Get TiddlyWiki Node.js running headlessly against a handful of vault notes. See if the filter syntax works on converted frontmatter. That's the proof of concept.

```bash
npm install tiddlywiki
npx tiddlywiki mywiki --init server
```

## See also

- [[README]]
- [[CONTRIBUTING]]
- [[zettelkasten]]
