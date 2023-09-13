---
tags:
  - databases
---

```dataview
table without id file.link as Game, maker as Maker, genre as Genre, year as Year, rating as Rating, last as "Last played"
from #games
where !contains(file.name, "Template")
sort last desc
```