---
tags:
  - categories
---

```base
display:
  file.name: Title
  property.status: Status
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
      - status
      - published

```