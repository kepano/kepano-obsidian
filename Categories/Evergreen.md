---
tags:
  - categories
---
An evergreen note is an idea. It doesn't have to be something that I agree with, but something is [[Composability|composable]]. In a way, every idiom is a kind of evergreen idea.

```dataview
table without id
	file.link as Name,
	created as Created
from #0🌲
where
	!contains(file.name,"Template")
sort created desc
```