---
category: "[[People]]"
tags:
  - people
  - musicians
created: {{date}}
---
## Albums

```dataview
table without id file.link as Album, artist as "Artist", rating as "Rating"
from #albums
where artist = this.file.link or contains(artist,this.file.link)
sort rating desc
```