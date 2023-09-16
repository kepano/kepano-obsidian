---
tags:
  - genres
---

```dataview
table without id
	file.link as Title,
	category as Category,
	rating as Rating
where
	contains(genre,this.file.link)
sort rating desc
```