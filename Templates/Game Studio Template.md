---
category:
  - "[[Companies]]"
tags:
  - companies
---
## Games

```dataview
table year as Year, rating as Rating
from #games
where maker = this.file.link or contains(maker,this.file.link)
sort year desc
```