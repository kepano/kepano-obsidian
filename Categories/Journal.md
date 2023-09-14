---
tags:
  - categories
---

```dataview
table without id
	file.link as Entry,
	created as Created
from #journal
where
	!contains(file.name,"Template")
sort created desc
```