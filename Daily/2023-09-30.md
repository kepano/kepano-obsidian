---
tags:
  - daily
---
## Notes

```dataview
list
where
	!contains(file.tags, "daily") and
	contains(file.outlinks, this.file.link) or
	contains(string(file.frontmatter), string(dateformat(this.file.day,"yyyy-MM-dd")))
sort file.ctime asc
limit 50
```