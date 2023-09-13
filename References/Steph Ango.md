---
category:
  - "[[People]]"
tags:
  - people
  - authors
org:
  - "[[Obsidian]]"
created: 2023-09-12
twitter: kepano
url: https://stephango.com/
---
## Clippings

```dataview
table without id
	file.link as Title,
	published as Published
where
	contains(author,this.file.link)
sort rating desc
```

## Meetings

```dataview
table without id
	file.link as Meeting,
	date as Date
where
	contains(people,this.file.link)
sort file.name desc
```

