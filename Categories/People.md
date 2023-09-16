---
tags:
  - categories
---

```dataview
table without id
	file.link as Person,
	filter(file.tags, (t) => t !="#people") as Tags 
where
  contains(category,this.file.link) and
  !contains(file.name,"Template")
sort file.name asc
```