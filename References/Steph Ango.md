---
category:
  - "[[People]]"
tags:
  - people
  - authors
company:
  - "[[Obsidian]]"
created: 2023-09-12
twitter: kepano
---
## Meetings

```dataview
table without id file.link as Meeting, date as Date
where contains(people,this.file.link)
sort file.name desc
```