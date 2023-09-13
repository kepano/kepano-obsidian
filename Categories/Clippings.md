---
tags:
  - categories
---

```dataview
table without id
	file.link as Title,
	author as Author,
	created as Clipped,
	published as Published
where
	contains(category,this.file.link) and
	!contains(file.name, "Template")
sort clipped desc
```