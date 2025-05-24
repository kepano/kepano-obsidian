---
tags:
  - categories
---

```base
display:
  file.name: Company
  property.url: Link
views:
  - type: table
    name: Table
    filters:
      and:
        - contains(categories, concat("[[", this.file.name, "]]"))
        - not(contains(file.name, "Template"))
    order:
      - file.name
      - url

```
