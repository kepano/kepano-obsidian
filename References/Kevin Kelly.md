---
category:
  - "[[People]]"
tags:
  - people
  - authors
created: 2023-09-12
---
## Books

```dataview
table without id
	file.link as Title,
	year as Year,
	rating as Rating
where
	contains(category,[[Books]]) and
	contains(author,this.file.link)
sort rating desc
```

# Clippings

```dataview
table without id
	file.link as Title,
	published as Published
where
	contains(category,[[Clippings]]) and
	contains(author,this.file.link)
sort rating desc
```

# Podcast episodes

```dataview
table without id
	file.link as Podcast,
	published as Published
where
	contains(category,[[Podcast episodes]]) and
	contains(guests,this.file.link)
sort rating desc
```