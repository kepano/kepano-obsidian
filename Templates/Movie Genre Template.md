---
tags:
  - movies/genres
---

```dataview
table without id
	file.link as Movie,
	rating as "Rating"
where
	contains(categories,[[Movies]]) and
	contains(genre,this.file.link)
sort rating desc
```