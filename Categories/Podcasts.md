---
related: "[[Podcast episodes]]"
---

```dataview
table without id
	file.link as Podcast, host as "Host"
where
  contains(category,this.file.link) and
  !contains(file.name,"Template")
sort file.name asc
```