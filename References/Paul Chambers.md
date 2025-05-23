---
categories:
  - "[[People]]"
tags:
  - people
  - musicians
created: 2023-09-13
---
## Albums

```dataview
table without id
	file.link as Album,
	artist as Artist,
	rating as Rating
where
	contains(categories,[[Albums]]) and
	contains(artist,this.file.link)
sort rating desc
```