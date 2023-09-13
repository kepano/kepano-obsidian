---
tags:
  - categories
---

```dataview
table without id
	file.link as Recipe, type as Type, author as Author, ingredients as Ingredients, rating as Rating
where
	contains(category,this.file.link) and
	!contains(file.name,"Template")
sort created desc
```