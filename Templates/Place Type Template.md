---
tags:
  - places/types
---

```leaflet
id: restaurants
linksTo: [[Pizzerias]]
minZoom: 3
maxZoom: 20
defaultZoom: 3
height: 400px
```

## Places

```dataview
table without id
	file.link as Place,
	rating as Rating,
	loc as Location
where
	contains(category, [[Places]]) and
	!contains(file.name,"Template") and 
	contains(type, this.file.link)
```