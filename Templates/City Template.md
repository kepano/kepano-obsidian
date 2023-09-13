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
table start as Start, end as End
from #trips
where contains(loc, this.file.link)
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
table rating as Rating, type as "Type"
from #places
where contains(loc, this.file.link)
sort rating desc
```