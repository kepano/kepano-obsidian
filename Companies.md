```dataview
table without id file.link as Company, people as People
from #companies
where !contains(file.name, "Template")
sort file.mtime desc
```