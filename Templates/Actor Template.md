---
category: "[[People]]"
type:
  - "[[Actors]]"
tags:
  - people
  - actors
---
## Movies

```dataview
table without id
	file.link as Movie,
	year as Year,
	rating as Rating
where
	contains(category,[[Movies]]) and
	contains(cast,this.file.link)
sort rating desc
```