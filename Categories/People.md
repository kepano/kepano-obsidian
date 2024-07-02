---
tags:
  - categories
---

```dataview
table without id
	file.link as Person,
	type as Type 
where
  contains(category,this.file.link) and
  !contains(file.name,"Template")
sort file.name asc
```