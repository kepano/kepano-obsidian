---
tags:
  - databases
---
```dataview
table without id file.link as Company, url as Link
from [[Companies]]
where !contains(file.name, "Template")
sort file.mtime desc
```