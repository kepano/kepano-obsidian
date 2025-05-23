---
categories:
  - "[[People]]"
tags:
  - people
  - directors
created: {{date}}
---
## Movies

```dataview
table without id
	file.link as Movie,
	year as Year,
	rating as Rating
where
	contains(categories,[[Movies]]) and
	contains(director,this.file.link)
sort rating desc
```