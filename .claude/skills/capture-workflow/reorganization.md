# Reorganization: split, merge, move, archive

## Split (note past ~300 lines or covering multiple topics)

Break into linked sub-notes, one topic each. Leave the original as a short overview linking to each sub-note, or redirect if the original topic no longer stands alone. Update the area MOC and `_system/index.md` for every resulting note.

## Merge (duplicates found)

Pick the note with the more complete history (usually the one with more links/updates) as the surviving note. Fold unique content from the other into it, preserving dates and details. Replace the losing note with nothing — move it to `90-Archive/` preserving its subpath, and update every reference to it (see link-refactor rule below). Note the merge in `_system/changelog.md`.

## Move / rename (misfiled note, or destination folder changed)

1. Move/rename the file.
2. **Mandatory link-refactor**: grep the entire vault (including `90-Archive/`) for wikilinks and markdown links to the old name/path, and update every reference to the new one.
3. Update `_system/index.md` and the relevant MOC(s) — old area loses the line, new area gains it.
4. Log the move in `_system/changelog.md`: `YYYY-MM-DD — move — old/path.md → new/path.md`.

## Archive (stale or completed)

Move to `90-Archive/`, preserving the original subpath (e.g. `10-Work/Projects/Foo.md` → `90-Archive/10-Work/Projects/Foo.md`). Run the same link-refactor and index/MOC update as a move. Archived notes remain searchable by retrieval — archiving is not deleting.

## Changelog format

`YYYY-MM-DD — split|merge|move|archive — details`, one line per change.
