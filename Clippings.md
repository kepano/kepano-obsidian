---
tags:
  - databases
---
```dataview
table without id file.link as Title, author as Author, created as Clipped, published as Published
from #clippings 
where !contains(file.name, "Template")
sort clipped desc
```