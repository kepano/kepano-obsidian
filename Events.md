---
tags:
  - databases
---
```dataview
table from #events 
where !contains(file.name,"Template")
```