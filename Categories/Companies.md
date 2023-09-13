---
tags:
  - categories
---

```dataview
table without id
	file.link as Company,
	url as Link
where
	contains(category,this.file.link)
	and !contains(file.name, "Template")
sort file.mtime desc
```