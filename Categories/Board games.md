---
tags:
  - categories
---

```dataview
table without id
	file.link as Game,
	rating as Rating,
	last as Last
where
  contains(category,this.file.link) and
  !contains(file.name,"Template")
```