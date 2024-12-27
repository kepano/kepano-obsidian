---
tags:
  - games/genres
---

```dataview
table without id
	file.link as Game,
	maker as Maker,
	year as Year,
	rating as Rating
where
	contains(category, [[Games]]) and
	!contains(file.name, "Template") and
	contains(genre, this.file.link)
sort rating desc
```
