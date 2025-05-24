---
tags:
  - categories
---

```base
display:
  file.name: Title
  property.author: Author
  property.created: Clipped
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
      - author
      - created
      - published
    sort:
      - column: clipped
        direction: DESC
```
