---
category:
  - "[[People]]"
tags:
  - people
  - directors
created: {{date}}
---
## Movies

```dataview
table without id file.link as Movie, year as "Year", ratingImdb as "Rating"
from #movies
where director = this.file.link or contains(director,this.file.link)
sort ratingImdb desc
```