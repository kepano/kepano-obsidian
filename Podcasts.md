---
related: "[[Podcast episodes]]"
---
```dataview
table without id file.link as Podcast, host as "Host"
from #podcast and !#episodes
where !contains(file.name,"Template")
sort file.name asc
```