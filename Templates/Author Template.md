---
category: "[[People]]"
type:
  - "[[Authors]]"
tags:
  - people
  - authors
---
## Books

```dataview
table without id
	file.link as Title,
	year as Year,
	rating as Rating
where
	contains(category,[[Books]]) and
	contains(author,this.file.link)
sort rating desc
```