---
tags:
  - databases
---
```leaflet
id: places
markerTag: places
maxZoom:15
height:50%
```

```dataview
table without id file.link as Place, location as "Location", type as Type, rating as "Rating"
from #places
where !contains(file.tags,"places/types") and !contains(file.name,"Template")
sort last desc
```