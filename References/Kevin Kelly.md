---
categories:
  - "[[People]]"
tags:
  - people
  - authors
created: 2023-09-12
---
## Books

![[Books.base#Author]]

# Clippings

```dataview
table without id
	file.link as Title,
	published as Published
where
	contains(categories,[[Clippings]]) and
	contains(author,this.file.link)
sort rating desc
```

# Podcast episodes

```dataview
table without id
	file.link as Podcast,
	published as Published
where
	contains(categories,[[Podcast episodes]]) and
	contains(guests,this.file.link)
sort rating desc
```