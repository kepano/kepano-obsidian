---
tags:
  - products/types
---

```dataview
table without id
	file.link as Item,
	maker as Maker,
	price as Price,
	rating as Rating,
	acquired as Acquired
where
	contains(categories, [[Products]]) and
	!contains(file.name,"Template") and 
	contains(type,this.file.link)
sort
	acquired desc,
	rating desc,
	file.mtime desc
```