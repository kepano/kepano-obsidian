# Attachment pipeline

1. Copy the binary into `_attachments/`, named `YYYY-MM-DD-description.ext` (real current date, kebab-case description).
2. Create or update a companion note in the correct folder (per `_system/conventions.md` frontmatter and the destination folder's `CLAUDE.md`):
   - Embed the file with `![[YYYY-MM-DD-description.ext]]`.
   - Summarize its contents as searchable text — read the PDF or describe the image so retrieval can find it by keyword, not just by filename.
   - List the path under the `attachments:` frontmatter key.
3. Link the companion note into the relevant MOC and any related notes, same as any other capture.
4. Update `_system/index.md` with the companion note's line.
