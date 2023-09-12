---
category: "[[People]]"
tags:
  - people
  - actors
---
## Movies

```dataview
table without id file.link as Movie, year as "Year", ratingImdb as "Rating"
from #movies
where cast = this.file.link or contains(cast,this.file.link)
sort ratingImdb desc
```