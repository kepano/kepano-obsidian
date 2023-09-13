My personal [Obsidian](https://obsidian.md/) vault structure. A bottom-up approach to note-taking and organizing things I am interested in. This is not dogma, just my personal approach. Hopefully it can serve as inspiration, but do what works for you!

To learn more about how I use Obsidian, visit my website [stephango.com](https://stephango.com/topics/obsidian/).

## Get started

1. [Download this vault](https://github.com/kepano/kepano-obsidian/archive/refs/heads/main.zip)
2. Unzip the .zip file to a folder of your choosing
3. Open Obsidian and create a new vault pointing to that folder

## Vault structure

### Theme and related tools

- My theme: [Minimal](https://github.com/kepano/obsidian-minimal), more at [minimal.guide](https://minimal.guide)
- My [web clipper](https://stephango.com/obsidian-web-clipper) for saving articles and pages on the web

### Plugins

Some of my templates depend on plugins I use:

- [Dataview](https://github.com/blacksmithgu/obsidian-dataview) for many database views
- [Periodic notes](https://github.com/liamcain/obsidian-periodic-notes) and [Calendar](https://github.com/liamcain/obsidian-calendar-plugin) for daily notes
- [Leaflet](https://github.com/javalent/obsidian-leaflet) for maps

### Folders

I use very few folders. My personal notes are primarily in the root, these are my journal entries. Folders are for everything else. I do not use the file explorer much for navigation, instead I navigate mostly using the quick switcher or clicking links.

The folders I use:

- **Attachments** for images, PDFs, etc.
- **Clippings** for articles and other pages captured with my [web clipper](https://stephango.com/obsidian-web-clipper) written by other people.
- **Daily** for my daily notes, all named `YYYY-MM-DD.md`.
- **References** for anything that refers to something that exists outside of my vault, e.g. books, movies, places, people, podcasts, etc.
- **Templates** for templates. In my real personal vault the "Templates" folder is nested under "Meta" which also contains my personal style guide and other random notes about the vault.

The following folders are not part of my personal system, but I have created them for the sake of clarity. The notes in these folders would be in the root of my personal vault:

- **Categories** contains top-level overviews of notes per category (e.g. books, movies, podcasts, etc).
- **Notes** contains example notes.

If you want to use this vault as a starting point the **Categories** and **Templates** folders contain everything that you need.

## Style guide
### Templates and metadata

I use templates very heavily, because they allow me to lazily insert most of the metadata I need about any kind of note.

The `.obsidian/types.json` file shows which properties are assigned to which types. 

- Most of my properties attempt to be reusable across categories
- Many properties have short names e.g. `start` instead of `startdate`
- I use the `list` type more than the `text` type for many properties, because I find it useful to be able to enter multiple links

### Categories and tagging

My notes are primarily organized using the category property, e.g. `category: "[[Movies]]"`. These also function as links that help me easily navigate to the overview note for that category. Some rules I personally follow:

- Always pluralize categories and tags
- Use `YYYY-MM-DD` everywhere
- Use a single vault for everything
- Avoid folders for organization
- Avoid non-standard Markdown

### Rating system

Anything with a `rating` uses an integer from 1 to 7

  - 7 — **Perfect**, must try, life-changing, go out of your way to seek this out
  - 6 — **Excellent**, worth repeating
  - 5 — **Good**, don't go out of your way, but enjoyable
  - 4 — **Passable**, works in a pinch
  - 3 — **Bad**, don't do this if you can
  - 2 — **Atrocious**, actively avoid, repulsive
  - 1 — **Evil**, life-changing in a bad way

Why this scale? I like the 7 scale better than 4 or 5 stars because I need more granularity at the top, for the good experiences, and 10 is too many.