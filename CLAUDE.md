# Second Brain — Vault Router

This vault is a personal knowledge base, operated through Claude Code and read in Obsidian.

## Vault map

- `00-Inbox/` — quick captures not yet filed.
- `10-Work/` — job/business: Projects, People, Meetings, Reference.
- `20-Personal/` — Health, Family, Finance, Home, Travel.
- `30-Knowledge/` — evergreen topic notes, not tied to work or personal admin.
- `40-Journal/` — daily notes, `YYYY-MM-DD.md`.
- `90-Archive/` — completed/stale notes, preserving original subpath. Never delete, archive.
- `_attachments/` — all binary files (images, PDFs, audio).
- `_staging/` — drop zone for bulk-importing existing notes/exports.
- `_templates/` — note templates.
- `_system/` — conventions, preferences, index, changelog.
- `Home.md` — top-level map of content. `Upcoming.md` — rolling deadlines/tasks.

## Intent routing

Workflows are defined in project skills, not in this file. Capturing information → `capture-workflow` skill. Answering questions from the vault → `retrieval-format` skill. Housekeeping → `vault-maintenance` skill. Mixed-intent messages may invoke multiple skills in one turn (capture before retrieve). If a message states a preference about answer style, edit `_system/preferences.md` (this is a capture).

## Hard rules (apply to every operation, regardless of skill)

- Always use the real current date (run `date` when uncertain — never guess or assume the date). Resolve relative dates in my messages to absolute YYYY-MM-DD.
- Never delete content; obsolete material moves to `90-Archive/`, preserving its subpath.
- Obsidian compatibility: plain markdown, `[[wikilinks]]` for internal links, `![[file.ext]]` for embeds, YAML frontmatter on every note, file names are note titles (Title Case, unique across the vault).
- Never store passwords, API keys, or full account numbers; store a pointer like "see password manager".
- Log every structural change (move/rename/merge/split/archive) as one line in `_system/changelog.md`.
- Read `_system/conventions.md` before modifying files; nested `CLAUDE.md` files override this one for their subtree.
- Be concise in chat; the durable output is the vault.
