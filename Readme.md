An Obsidian vault containing my vault structure, as well as my templates and settings. See also [my theme Minimal](https://github.com/kepano/obsidian-minimal).

## Plugins

Some of my templates depend on plugins I use:

- [Dataview](https://github.com/blacksmithgu/obsidian-dataview) for many database views
- [Periodic notes](https://github.com/liamcain/obsidian-periodic-notes) for my daily notes
- [Leaflet](https://github.com/javalent/obsidian-leaflet) for maps

## Folder structure

I use very few folders. I keep the root of my vault directory for things that I have created, such as journal entries

- **Attachments** for images, PDFs, etc
- **Clippings** for articles and other pages captured with my [Web Clipper](https://stephango.com/obsidian-web-clipper)
- **Daily** for my daily notes, all in `YYYY-MM-DD.md` format
- **References** for anything that refers to something that exists outside of my vault, e.g. books, movies, places, people, podcasts, etc.
- **Templates** for templates. This is actually nested under "Meta" in my personal vault, but I've moved it to the top-level for clarity. Meta also contains my personal style guide and other random things that are about the vault.

## Templates and metadata

The `.obsidian/types.json` file shows which properties are assigned to which types. Many have short names that are meant for me to remember, e.g. `start` instead of `startdate`.

## Categories and tagging

I primarily use the category property, e.g. `category: [[Movies]]` to organize and navigate my vault. Some rules I personally follow:

- Always pluralize categories and tags
- Use `YYYY-MM-DD` everywhere
- Never use folders for organization
- Single vault for everything
- Avoid non-standard Markdown

## Rating system

Anything with a `rating` uses an integer from 1 to 7

  - 7 — **Perfect**, must try, life-changing, go out of your way to seek this out
  - 6 — **Excellent**, worth repeating
  - 5 — **Good**, don't go out of your way, but enjoyable
  - 4 — **Passable**, works in a pinch
  - 3 — **Bad**, don't do this if you can
  - 2 — **Atrocious**, actively avoid, repulsive
  - 1 — **Evil**, life-changing in a bad way

Why this scale? I like the 7 scale better than 4 or 5 stars because I need more granularity at the top, for the good experiences, and 10 is too many.