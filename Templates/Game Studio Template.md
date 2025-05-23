---
categories:
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
	contains(categories,[[Games]]) and
	contains(maker,this.file.link)
sort year desc
```