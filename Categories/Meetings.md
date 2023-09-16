---
tags:
  - categories
---

```dataview
table without id
	file.link as Meeting,
	type as Type,
	people as People,
	date as Date
where 
	contains(category,this.file.link) and
	!contains(file.name,"Template")
sort date desc
limit 100
```