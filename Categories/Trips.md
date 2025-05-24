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
  file.name: Name
  property.loc: Location
  property.end: End
  property.start: Start
views:
  - type: table
    name: Table
    order:
      - file.name
      - loc
      - start
      - end
```
