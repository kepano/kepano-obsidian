---
category: "[[People]]"
tags:
  - people
  - authors
---
## Books

```dataview
table without id file.link as Title, year as "Year", rating as "Rating"
from #books
where author = this.file.link or contains(author,this.file.link)
sort rating desc
```