---
related: "[[Podcast episodes]]"
---

```base
display:
  file.name: Podcast
  property.host: Host
views:
  - type: table
    name: Table
    filters:
      and:
        - contains(categories, concat("[[", this.file.name, "]]"))
        - not(contains(file.name, "Template"))
    order:
      - file.name
      - host
```

