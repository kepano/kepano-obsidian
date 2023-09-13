---
tags:
  - databases
---
```dataview
table without id file.link as Game, rating as Rating, last as Last
where contains(category,[[Board games]]) and !contains(file.name,"Template")
```