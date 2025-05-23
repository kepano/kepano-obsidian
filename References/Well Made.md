---
categories:
  - "[[Podcasts]]"
host:
  - "[[Steph Ango]]"
rating: 
tags:
  - podcast
---
## Episodes

```dataview
table without id
	link(file.link, "Ep. " + string(episode)) as Episode,
	guests as Guest,
	rating as Rating
where
	contains(categories,[[Podcast episodes]]) and
	contains(show,this.file.link)
sort episode desc
```