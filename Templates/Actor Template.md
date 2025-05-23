---
categories: "[[People]]"
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
	contains(categories,[[Movies]]) and
	contains(cast,this.file.link)
sort rating desc
```