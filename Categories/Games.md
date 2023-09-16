---
tags:
  - categories
---

```dataview
table without id
	file.link as Game,
	maker as Maker,
	genre as Genre,
	year as Year,
	rating as Rating,
	last as "Last played"
where
	contains(category,this.file.link) and
	!contains(file.name, "Template")
sort last desc
```
