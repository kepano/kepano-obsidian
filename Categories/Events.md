---
tags:
  - categories
---

```base
filters:
  and:
    - contains(categories, concat("[[", this.file.name, "]]"))
    - not(contains(file.name, "Template"))
display:
  file.name: Event
  property.type: Type
  property.start: Start
  property.loc: Location
views:
  - type: table
    name: Table
    order:
      - file.name
      - loc
      - type
      - start

```