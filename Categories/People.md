---
tags:
  - categories
---

```base
filters:
  and:
    - contains(property.categories, "[[People]]")
    - not(contains(file.name, "Template"))
display:
  file.name: Name
  property.tags: Tags
views:
  - type: table
    name: Table
    order:
      - file.name
      - tags

```