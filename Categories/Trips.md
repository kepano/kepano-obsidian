---
tags:
  - categories
---

```dataview
table without id
	file.link as Trip,
	loc as Location,
	start as Start,
	end as End
where
	contains(category,this.file.link) and
	!contains(file.name, "Template") and
	!contains(file.name, "Planning")
sort start desc
```
