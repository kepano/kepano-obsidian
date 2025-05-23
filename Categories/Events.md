---
tags:
  - categories
---

```dataview
table without id
	file.link as Event
where
  contains(categories,this.file.link) and
  !contains(file.name,"Template")
```