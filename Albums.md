---
tags:
  - music
  - databases
---
```dataview
table without id file.link as Album, artist as Artist, rating as Rating, year as Year, genre as Genre
from #albums
where !contains(file.name, "Template")
sort rating desc
```