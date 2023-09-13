---
tags:
  - music/genres
---

```dataview
table without id
	file.link as Album,
	artist as Artist,
	genre as Genre,
	rating as Rating
where
	contains(category, [[Albums]]) and
	contains(genre,this.file.link)
sort rating desc
```