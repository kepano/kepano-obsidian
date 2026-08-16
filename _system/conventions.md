# Conventions

Single source of truth for naming, tagging, frontmatter, and linking. Read before modifying any file. Nested `CLAUDE.md` files may add to this for their subtree but should not contradict it.

## Frontmatter schema

Every note gets YAML frontmatter:

```yaml
---
created: YYYY-MM-DD
updated: YYYY-MM-DD
type: note | project | person | meeting | journal | reference | attachment-note
tags: []
aliases: []
status: (projects only — active | waiting | done)
attachments: [] (only if any)
---
```

- `aliases` (person/entity notes only): every name variant, nickname, email, or handle they might be referenced by, e.g. `aliases: [Sarah, Sarah Chen, sarah@acme.com]`. Add new aliases as they appear in later captures.
- `updated` must be bumped on every edit.
- All dates are real calendar dates — resolve relative phrasing ("next Friday", "in two weeks") to absolute `YYYY-MM-DD` at capture time. Run `date` if unsure; never guess.

## Tasks with dates

Anything with a due/expiry/follow-up date is a task, not just a fact:

```markdown
- [ ] Renew passport 📅 2027-03-01
```

Tasks live in their topical note AND get a linked line in `Upcoming.md`. When a task is done, check the box in the source note and remove the line from `Upcoming.md`.

## Naming

- Notes: Title Case, unique across the vault. The file name is the note title.
- Journal notes: `YYYY-MM-DD.md`.
- Meeting notes: `YYYY-MM-DD Meeting - Topic.md`.
- Attachments: `YYYY-MM-DD-description.ext` (kebab-case description).

## Tagging

Small controlled vocabulary, lowercase, hyphenated. Prefer links over tags — a tag is for broad category filtering, a link is for a specific relationship. Starter tag set: `#project`, `#person`, `#meeting`, `#idea`, `#reference`, `#health`, `#finance`, `#home`, `#travel`, `#recurring`.

## Linking

- Minimum one wikilink per note.
- MOCs (maps of content) link down to topic/area notes. Notes link laterally to related notes.
- On any move/rename, grep the entire vault for wikilinks and markdown links to the old name/path and update every reference (see `reorganization.md` in the capture-workflow skill).
