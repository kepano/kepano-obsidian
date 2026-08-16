---
name: vault-maintenance
description: Use when the user asks for vault housekeeping — weekly review, process the inbox, find duplicates or orphan notes, fix broken links, archive stale notes, audit frontmatter/naming, or rebuild MOCs. Also triggers on import requests ("import my notes", "process the staging folder", "migrate my old notes") and upcoming-list requests ("what's overdue", "update the upcoming list"). Can be run manually as /vault-maintenance.
---

# Vault maintenance

Destructive bulk operations (merges, archiving multiple notes, bulk moves) must always list the planned changes and get explicit confirmation before executing. Non-destructive operations (rebuilding the index, regenerating Upcoming.md) can proceed directly.

## Inbox processing

For each note in `00-Inbox/`: classify → move to the right folder (apply capture-workflow rules: template, frontmatter, aliases) → link into related notes and the area MOC → update `_system/index.md` → remove from inbox.

## Bulk import (`_staging/`)

If `_staging/` contains files (exports from Apple Notes, docs, old vaults, spreadsheets, etc.), process them in batches through capture-workflow rules:

1. Split multi-topic files into proper single-topic notes.
2. File each into the right folder with frontmatter, links, aliases, and index entries.
3. Move any binaries to `_attachments/` with companion notes (see `attachments.md` in capture-workflow).
4. Move processed originals to `90-Archive/_staging-originals/` so nothing is lost.
5. `_staging/` ends empty.

List the batch plan and confirm before processing more than a few files at once.

## Regenerate `Upcoming.md`

Scan the vault for unchecked `- [ ]` items with a 📅 date. Group by month. Link each to its source note. Flag overdue items at the top. Drop completed (checked) items.

## Rebuild `_system/index.md`

Walk every note in the vault, rebuild `title | type | tags | updated` from scratch, fixing any drift from incremental updates.

## Orphan and staleness checks

- Orphan notes: no incoming or outgoing links. Flag for review — don't auto-archive.
- Stale notes: not updated in 90+ days. Propose archiving; confirm before moving.
- Duplicate detection: similar titles/content covering the same entity or topic. Propose a merge; confirm before executing (see `reorganization.md` in capture-workflow for the merge procedure).

## Frontmatter and naming audit

Check every note against `_system/conventions.md`: required frontmatter keys present, dates real and absolute, naming conventions followed, `aliases` present on person/entity notes. Fix drift directly; log fixes in `_system/changelog.md`.

## MOC rebuild

For each area MOC, verify it links every current note in its area and no longer links archived/removed ones.

## Broken links

See `link-repair.md` in this skill folder for the detailed procedure.
