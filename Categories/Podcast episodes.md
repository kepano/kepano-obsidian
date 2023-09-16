---
tags:
  - categories
---

```dataview
table without id
	link(file.link, "Ep. " + string(episode)) as Episode,
	show as Show,
	guests as Guest,
	episode as Ep,
	rating as Rating,
	published as "Published"
where
	contains(category,this.file.link) and
	!contains(file.name, "Template")
sort published desc
```