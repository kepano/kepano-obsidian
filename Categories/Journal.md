---
tags:
  - categories
---

```base
filters:
  and:
    - contains(property.tags, "journal")
    - not(contains(file.name, "Template"))
display:
  file.name: Entry
  property.created: Created
views:
  - type: table
    name: Table
    order:
      - file.name
      - created

```
