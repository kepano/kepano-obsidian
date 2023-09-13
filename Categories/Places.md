---
tags:
  - categories
---
```leaflet
id: places
markerTag: places
maxZoom:15
height:400px
```

## Places

```dataview
table without id
	file.link as Place,
	loc as Location,
	type as Type,
	rating as Rating
where
	contains(category,this.file.link) and
	!contains(file.tags,"places/types") and
	!contains(file.name,"Template")
sort last desc
```