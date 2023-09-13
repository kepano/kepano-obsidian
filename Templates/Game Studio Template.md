---
category:
  - "[[Companies]]"
tags:
  - companies
---
## Games

```dataview
table without id
	file.link as Game,
	year as Year,
	rating as Rating
where
	contains(category,[[Games]]) and
	contains(maker,this.file.link)
sort year desc
```