---
name: capture-workflow
description: Use whenever the user provides information to store — declarative statements of fact, "note that", "remember this", "save this", "add to", pasted content, dropped files/images/PDFs, meeting summaries, or corrections to stored info ("actually it's X not Y"). Covers filing, note creation/editing, linking, reorganization, and attachments. Do NOT use for questions about existing information — that is retrieval-format.
user-invocable: false
---

# Capture workflow

Tight checklist. Don't write essays into notes — file them.

1. Classify the content type: fact, project update, person, meeting, journal entry, document, idea, preference, task/deadline.
2. Preference about answer style? → edit `_system/preferences.md`, confirm in one line, done.
3. **Search the vault first** for an existing home: grep title keywords + synonyms, check `_system/index.md` and the relevant MOC. Prefer appending/updating over creating a new note.
4. If creating: pick the destination folder (read its `CLAUDE.md`), use the matching `_templates/` template, fill frontmatter per `_system/conventions.md`.
5. **Stamp real dates everywhere.** Run `date` if unsure — never guess. Use the actual current date for `created`/`updated` frontmatter. Resolve relative dates in my message ("next Friday", "in two weeks", "last month") into absolute `YYYY-MM-DD`, keeping my phrasing if useful ("follow up next Friday (2026-07-17)").
6. **Anything with a due/expiry/follow-up date is a task, not just a fact.** Record it in the relevant note as `- [ ] description 📅 YYYY-MM-DD`. Also add a matching line to `Upcoming.md` under the right month, linking back to the source note. When told something is done, check the box in the source note and remove it from `Upcoming.md`.
7. **Person/entity notes get an `aliases` frontmatter list** — every name variant, nickname, email, or handle they might be referenced by. Add new aliases as they appear in later captures.
8. Weave links: add `[[wikilinks]]` to every related existing note; add backlinks in those notes where natural; update the area MOC; update `Home.md` only if a new major area appeared.
9. **Update `_system/index.md`**: add a line for every new note (`title | type | tags | updated`); update the line on renames/moves.
10. Attachment involved? → follow `attachments.md` in this skill folder.
11. Note grew past ~300 lines, duplicates found, or content is misfiled? → follow `reorganization.md`.
12. Unclear where it belongs? → file in `00-Inbox/` with a one-line "needs filing" marker.
13. Confirm to the user in 1–2 lines: what was stored, where, what was linked.
