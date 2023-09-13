---
category:
  - "[[People]]"
tags:
  - people
  - authors
created: 2023-09-12
---
## Books

```dataview
table without id file.link as Title, year as "Year", rating as "Rating"
from #books
where author = this.file.link or contains(author,this.file.link)
sort rating desc
```

# Clippings

```dataview
table without id file.link as Title, published as Published
from #clippings
where author = this.file.link or contains(author,this.file.link)
sort rating desc
```

# Podcast episodes

```dataview
table without id file.link as Podcast, published as Published
from #episodes
where contains(guests,this.file.link)
sort rating desc
```