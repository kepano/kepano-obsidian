---
tags:
  - categories
---
An evergreen note is an idea. It doesn't have to be something that I agree with, but something is [[Composability|composable]]. In a way, every idiom is a kind of evergreen idea.

```base
display:
  file.name: Name
  property.created: Created
views:
  - type: table
    name: Table
    filters:
      and:
        - contains(property.tags, "0🌲")
        - not(contains(file.name, "Template"))
    order:
      - file.name
      - created
```