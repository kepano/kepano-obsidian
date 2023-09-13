---
tags:
  - databases
---
```dataview
table without id file.link as Event
from #events 
where !contains(file.name,"Template")
```