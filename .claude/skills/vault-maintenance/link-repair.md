# Broken-link repair

1. Enumerate every `[[wikilink]]` and `[markdown](link)` across all `.md` files, including `90-Archive/`.
2. For each, check the target exists at that path/title. A wikilink target is a note title (unique across the vault) — resolve it the way Obsidian would (exact title match, case-insensitive fallback).
3. Broken target candidates, in order of preference:
   - Exact title now living at a different path (was moved/archived without a logged rename) → repoint the link to the new path.
   - Title changed slightly (typo, pluralization) → repoint if confident, otherwise flag for the user.
   - Note genuinely gone (never existed, or content was merged elsewhere per `_system/changelog.md`) → repoint to the surviving note if the changelog shows a merge, otherwise flag as a true broken link.
4. List all proposed repairs before applying more than a handful — confirm with the user.
5. Log each repair in `_system/changelog.md`.

## Rename-refactor procedure (also used by capture-workflow's move/rename step)

On any note rename or move: grep the whole vault for the old title/path as both a wikilink and a markdown link, replace every occurrence with the new title/path, then re-run the broken-link scan above to confirm zero references to the old name remain.
