---
tags:
  - genres
---

```dataview
table without id
	file.link as Title,
	categories as categories,
	rating as Rating
where
	contains(genre,this.file.link)
sort rating desc
```