---
tags:
  - categories
---

```base
display:
  file.name: Podcast
  property.show: Show
  property.guests: Guests
  property.episode: Episode
  property.rating: Rating
  property.published: Published
views:
  - type: table
    name: Table
    filters:
      and:
        - contains(categories, concat("[[", this.file.name, "]]"))
        - not(contains(file.name, "Template"))
    order:
      - file.name
      - show
      - guests
      - episode
      - rating
      - published
```