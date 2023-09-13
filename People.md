---
tags:
  - databases
---
```dataview
table without id file.link as Person, filter(file.tags, (t) => t !="#people") as Tags
from #people 
where !contains(file.name,"Template") and !contains(file.tags,"people/type")
sort file.name asc
```