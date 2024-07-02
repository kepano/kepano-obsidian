---
tags:
  - categories
---

```dataview
table without id
	file.link as Product,
	rating as Rating,
	acquired as Acquired,
	type as Type,
	maker as Maker
where
	!contains(file.name, "Template") and
	contains(category, [[Products]])
sort
	acquired desc,
	file.name,
	rating desc,
	file.mtime desc
```
