---
tags:
  - music
  - categories
---

```dataview
table without id
	file.link as Album,
	artist as Artist,
	rating as Rating,
	year as Year,
	genre as Genre
where
	contains(category,this.file.link) and
	!contains(file.name, "Template")
sort rating desc
```