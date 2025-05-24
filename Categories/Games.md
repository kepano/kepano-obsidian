---
tags:
  - categories
---


```base
display:
  file.name: Book
  property.year: Year
  property.maker: Maker
  property.rating: Rating
  property.genre: Genre
  property.last: Last played
views:
  - type: table
    name: Table
    filters:
      and:
        - contains(property.categories, "[[Games]]")
        - not(contains(file.name, "Template"))
    order:
      - file.name
      - maker
      - genre
      - year
      - rating
      - last
```
