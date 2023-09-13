---
tags:
  - databases
---
```dataview
table rating as Rating, last as Last
where contains(category,[[Board games]]) and !contains(file.name,"Template")
```