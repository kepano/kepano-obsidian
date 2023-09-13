---
tags:
  - meetings/type
---


```dataview
table without id
	file.link as Meeting,
	people as People,
	date as Date
where
	contains(category, [[Meetings]]) and
	!contains(file.name,"Template") and 
	contains(type,this.file.link)
sort date desc
limit 50
```