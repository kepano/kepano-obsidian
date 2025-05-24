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

```base
filters:
  and:
    - contains(property.categories, "[[Places]]")
    - not(contains(file.name, "Template"))
display:
  property.type: Type
  property.rating: Rating
  property.loc: Location
  file.name: Name
views:
  - type: table
    name: Table
    order:
      - file.name
      - loc
      - type
      - rating
    sort:
      - column: property.loc
        direction: ASC

```
