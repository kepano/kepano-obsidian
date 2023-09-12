---
category:
  - "[[People]]"
tags:
  - people
birthday: 
company: []
created: {{date}}
---
## Meetings

```dataview
table without id file.link as Meeting, date as Date
where contains(people,this.file.link)
sort file.name desc
```