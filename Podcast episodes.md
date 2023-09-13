---
tags:
  - databases
---
```dataview
table without id link(file.link, "Ep. " + string(episode)) as Episode, show as "Show", guests as "Guest", episode as Ep, rating as "Rating", published as "Published"
from #podcast and #episodes
where !contains(file.name, "Template")
sort published desc
```