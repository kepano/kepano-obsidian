```dataview
table without id file.link as Title, clipped as "Clipped", published as Published
from #clippings 
where !contains(file.name, "Template")
sort clipped desc
```