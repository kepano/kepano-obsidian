---
tags:
  - movies/genres
---
```dataview
table ratingImdb as "Rating"
from #reference
where genre = this.file.link or contains(genre,this.file.link)
sort ratingImdb desc
```