---
created: 2026-08-15
updated: 2026-08-15
type: reference
tags: [vault, meta]
---

# How to use your Second Brain

## Adding information — just state it

No command needed. Declarative statements route to capture automatically:

- "Garvit and I are picking up doubles pickleball on Fridays now"
- "Note that the Tesla's registration renews March 2027"
- "Here's the receipt from dinner" (with a dropped file/image)
- "Actually, the meeting got moved to Thursday" (corrections update existing notes)

## Retrieving — just ask

Questions route to retrieval automatically:

- "What do I know about the DR project?"
- "When does my Tesla's registration renew?"
- "Summarize everything about EWOK"
- "Do I have anything on restaurants I went to with Manya?"
- Time-based questions work too: "What did I decide last month?" / "What's coming up in the next two weeks?" / "What's overdue?"

## Deadlines and follow-ups — state them like anything else

Anything with a date becomes a tracked task automatically:

- "My passport expires March 2027" → checkbox task in the passport note + a line in [[Upcoming]]
- "Follow up with Archana next week" → resolved to a real date and tracked
- "I renewed the passport" → the task gets checked off and leaves Upcoming

## Restaurant visits — your own pattern

You asked for this one specifically: mention a restaurant visit ("went to X with Manya, here's the receipt") and it becomes a note in `20-Personal/Dining/` from `_templates/restaurant-visit.md`, with the receipt attached and everyone you went with linked.

## Importing existing notes — use the staging folder

Export from Apple Notes, Google Docs, old vaults, etc., drop the files into `_staging/`, then say "import my staging folder." Files are split into proper notes, filed, linked, and the originals archived. Do this in batches if you have a lot.

## Capturing from your phone

Sync this folder (iCloud, Obsidian Sync, or git) and open it in Obsidian mobile. Jot quick notes into `00-Inbox/` from anywhere — no special format needed. Next time you're in Claude Code, say "clean up my inbox" and everything gets filed properly.

## Changing how answers look — just say so

These edit `_system/preferences.md` and stick permanently:

- "Keep answers shorter" / "Always use bullet points" / "For finance questions, always include dates and amounts"

## Maintenance — ask or run the command

- "Clean up my inbox" / "Do a weekly review" / "Find broken links" — or type `/vault-maintenance`

## Tips

- Mixed messages work: "Sarah moved to Portland — do I have anything else on her?" stores and searches in one turn.
- When unsure where something went, ask "where did you file that?"
- Open the folder in Obsidian anytime — graph view shows how notes connect.
- Nothing is ever deleted, only archived to `90-Archive/`.
