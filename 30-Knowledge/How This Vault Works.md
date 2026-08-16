---
created: 2026-08-15
updated: 2026-08-15
type: reference
tags: [vault, meta]
---

# How This Vault Works

This vault is a Second Brain: an Obsidian vault operated through Claude Code. Every message falls into one of three intents, routed automatically by [[Home|the skills defined in .claude/skills/]]:

- **Capture** — stating a fact, correction, or new information. Filed with frontmatter, wikilinks, and an index entry.
- **Retrieve** — asking a question. Answered by searching `_system/index.md`, grepping the vault, and following links.
- **Maintain** — housekeeping like inbox processing, import, or link repair.

Notes use plain markdown with YAML frontmatter (`created`, `updated`, `type`, `tags`, and sometimes `aliases`, `status`, `attachments`) and `[[wikilinks]]` to connect related ideas — that's what makes the [[Home|graph view]] in Obsidian meaningful instead of a flat pile of files. See `_system/conventions.md` for the full schema.

Sources: [[Home]], [[Knowledge MOC]]
