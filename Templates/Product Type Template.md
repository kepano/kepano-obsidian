---
tags:
  - products/types
---
```dataview
table without id
	file.link as Item, maker as "Maker", price as "Price", rating as Rating, purchased as Purchased
from #products
where type = this.file.link or contains(type,this.file.link)
sort purchased desc, rating desc, file.mtime desc
```