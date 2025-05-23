---
categories:
  - "[[Places]]"
type:
  - "[[Cities]]"
tags:
  - places
  - cities
loc: 
rating: 
created: {{date}}
last: 
location:
  - "35.021041"
  - "135.7556075"
---
## Trips

```dataview
table without id
	file.link as Trip,
	start as Start,
	end as End
where
	contains(categories, [[Trips]]) and
	contains(loc, this.file.link)
sort file.name desc
```

## Map

```leaflet
id: kyoto
minZoom: 10
maxZoom: 20
defaultZoom: 12
markerTag:
  - places
height: 400px
coordinates: [[Kyoto]]
```

## Places

```dataview
table without id
	file.link as Place,
	rating as Rating,
	type as Type
where
	contains(categories, [[Places]]) and
	contains(loc, this.file.link)
sort rating desc
```