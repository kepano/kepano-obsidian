---
tags:
  - categories
---

```base
display:
  file.name: Game
  property.rating: Rating
  property.last: Last
views:
  - type: table
    name: Table
    filters:
      and:
        - contains(categories, concat("[[", this.file.name, "]]"))
        - not(contains(file.name, "Template"))
    order:
      - file.name
      - rating
      - last

```