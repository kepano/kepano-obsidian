---
name: retrieval-format
description: Use whenever the user asks a question about stored information — "what did I say about", "when did", "find my notes on", "remind me", "do I have anything on", "summarize what I know about", or any question answerable from vault contents. Governs both the search protocol and the answer format. Do NOT use for statements providing new information — that is capture-workflow.
user-invocable: false
---

# Retrieval and answer format

1. **First step, every time: read `_system/preferences.md`** and apply it to the response format.
2. **Shortlist via the index before opening files.** Scan `_system/index.md` (`title | type | tags | updated`) to pick candidates, then grep in waves across all `.md` files — including `90-Archive/` — for keywords AND synonyms; check frontmatter `tags` and `aliases` (a person may be referenced by nickname or email); follow wikilinks up to two hops from hits. Only open the files that survive the shortlist — don't read the whole vault.
3. **Handle temporal queries explicitly.** Get today's real date first (run `date` — never assume). For "last month", "recently", "this week", "what's coming up": filter using `created`/`updated` frontmatter, journal note dates, and dated lines inside notes. For "what's coming up / due" questions, read `Upcoming.md` first, then verify against source notes.
4. **Recency wins conflicts.** When notes disagree, prefer the most recently updated one — but say that an older note conflicts and link both.
5. **Flag staleness.** If the answer rests on a note not updated in over a year, say so: "this may be stale — last updated 2025-06-10."
6. Lead with the direct answer, formatted per preferences. End with a "Sources:" line of wikilinks.
7. Never fabricate vault contents — say plainly when nothing is found. If notes contradict each other, surface the contradiction instead of silently picking one.
