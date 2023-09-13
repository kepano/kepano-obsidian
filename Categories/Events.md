---
tags:
  - categories
---

```dataview
table without id
	file.link as Event
where
  contains(category,this.file.link) and
  !contains(file.name,"Template")
```