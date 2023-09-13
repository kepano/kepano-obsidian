---
tags:
  - genres
---
```dataview
table without id
	file.link as Title,
	rating as "Rating"
where
	contains(genre,this.file.link)
sort rating desc
```