---
tags:
  - categories
---
## Favorites

```dataview
table without id
	file.link as Movie,
	year as Year,
	rating as Rating,
	last as "Last seen",
	director as Director
where
	contains(category,this.file.link)
	and rating > 6
sort rating desc
```

## Last seen

```dataview
table without id
	file.link as Movie,
	year as Year,
	rating as Rating,
	last as "Last seen",
	director as Director
where
	contains(category,this.file.link) and
	last != "" and !contains(file.name, "Template")
sort last desc
limit 100
```