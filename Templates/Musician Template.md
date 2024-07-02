---
category: "[[People]]"
type:
  - "[[Musicians]]"
tags:
  - people
  - musicians
created: {{date}}
---
## Albums

```dataview
table without id
	file.link as Album,
	artist as Artist,
	genre as Genre,
	rating as Rating
where
	contains(category,[[Albums]]) and
	contains(artist,this.file.link)
sort rating desc
```