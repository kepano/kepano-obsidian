---
tags:
  - people/types
---
```dataview
table without id
	file.link as Name
from #people
where
	!contains(file.name,"Template")
sort file.name asc
```