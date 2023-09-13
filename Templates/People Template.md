---
category:
  - "[[People]]"
tags:
  - people
birthday: 
org: []
created: {{date}}
---
## Meetings

```dataview
table without id file.link as Meeting, date as Date
from #meetings
where contains(people,this.file.link)
sort file.name desc
```