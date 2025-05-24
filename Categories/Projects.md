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
  property.status: Status
  property.url: URL
  file.name: Name
  property.type: Type
  property.year: Year
views:
  - type: table
    name: Table
    order:
      - file.name
      - type
      - year
      - status
      - url

```
