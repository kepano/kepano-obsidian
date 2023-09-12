---
tags:
  - people/types
---
```dataview
table without id file.link as Name
from #actors
where !contains(file.name,"Template")
sort file.name asc
```