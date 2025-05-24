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
  file.name: Meeting
  property.type: Type
  property.people: People
  property.date: Date
views:
  - type: table
    name: Table
    order:
      - file.name
      - type
      - people
      - date

```
