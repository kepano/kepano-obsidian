---
tags:
  - categories
---

```dataview
table without id
	file.link as Book,
	author as Author,
	year as Year,
	rating as Rating,
	created as Added,
	genre as Genre
where
	contains(category,this.file.link) and
	!contains(file.name, "Template")
sort rating desc, date asc
```
