---
categories:
  - "[[People]]"
tags:
  - people
birthday: 
org: []
created: {{date}}
---
## Meetings

```dataview
table without id
	file.link as Meeting,
	date as Date
where
	contains(categories,[[Meetings]]) and
	contains(people,this.file.link)
sort file.name desc
```