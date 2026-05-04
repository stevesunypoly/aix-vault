-----

## name: dump
description: export this conversation as a markdown file with YAML frontmatter, download link provided immediately

When I type `//dump`, do the following with no commentary, no questions, no preamble:

1. Collect conversation metadata:
- title: the conversation title or first human message truncated to 60 chars
- date: today’s date in YYYY-MM-DD
- conversation_id: extract from the current URL if available, otherwise “unknown”
- model: the model in use (claude-sonnet-4-6 unless you know otherwise)
- contributor: Steve
1. Generate the full conversation transcript from this session in this format:

```
---
type: claude_conversation
title: "{title}"
conversation_id: "{conversation_id}"
contributor: Steve
model: "{model}"
date: "{date}"
source: claude.ai
exported: "{datetime now in ISO 8601}"
tags:
  - claude
  - incoming
---

# {title}

**Date:** {date}
**Model:** {model}

---

{for each turn:}
**H:** {human message text}

**A:** {assistant message text}

---
```

1. Write the file to `/home/claude/` named `{YYYY-MM-DD}-{slugified-title}.md`
- slugify: lowercase, spaces to hyphens, remove special chars, max 60 chars
1. Copy it to `/mnt/user-data/outputs/`
1. Call `present_files` with the output path so a download link appears immediately.

That is all. One file. One download link. No sorting. Destination: Steve’s incoming folder.