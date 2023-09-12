---
previous: "[[{{date-1d}}]]"
next: "[[{{date+1d}}]]"
tags:
  - daily
---
## Notes

```dataview
list
where
	!contains(file.tags, "daily") and
	contains(file.outlinks, this.file.link) or
	contains(string(file.frontmatter), string(this.file.day))
sort file.ctime asc
limit 50
```