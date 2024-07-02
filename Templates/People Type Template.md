---
tags:
  - people/types
---

```dataview
table without id
	file.link as Name
where
	contains(category, [[People]]) and
	!contains(file.name,"Template") and
	contains(type,this.file.link)
sort file.name asc
```