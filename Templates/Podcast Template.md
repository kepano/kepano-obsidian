---
category:
  - "[[Podcasts]]"
host: []
rating: 
tags:
  - podcast
---
## Episodes

```dataview
table without id link(file.link, "Ep. " + string(episode)) as Episode, guest as "Guest", rating as "Rating"
from #podcast and #episodes
where show = this.file.link
sort episode desc
```