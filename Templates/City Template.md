---
category:
  - "[[Places]]"
type:
  - "[[Cities]]"
tags:
  - places
  - cities
location: 
rating: 
created: {{date}}
last: 
---
## Trips

```dataview
table without id
	file.link as Trip,
	start as Start,
	end as End
where
	contains(category, [[Trips]]) and
	contains(location, this.file.link)
sort file.name desc
```

## Places

```leaflet
id: madrid
minZoom: 10
maxZoom: 20
defaultZoom: 12
linksTo: [[Madrid]]
height: 50%
coordinates: [[Madrid]]
```

```dataview
table without id
	file.link as City,
	rating as Rating,
	type as Type
where
	contains(category, [[Places]]) and
	contains(location, this.file.link)
sort rating desc
```