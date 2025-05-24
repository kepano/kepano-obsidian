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
  property.rating: Rating
  property.last: Last
views:
  - type: table
    name: Table
    order:
      - file.name
      - rating
      - last

```
