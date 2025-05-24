---
tags:
  - music
  - categories
---

```base
display:
  file.name: Album
  property.year: Year
  property.artist: Artist
  property.created: Added
  property.rating: Rating
  property.genre: Genre
views:
  - type: table
    name: Table
    filters:
      and:
        - contains(categories, concat("[[", this.file.name, "]]"))
        - not(contains(file.name, "Template"))
    order:
      - file.name
      - artist
      - rating
      - year
      - genre

```