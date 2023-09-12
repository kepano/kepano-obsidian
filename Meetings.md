```dataview
table without id file.link as Meeting, type as Type, people as People, date as Date
from #meetings
where !contains(file.name,"Template")
sort date desc
limit 100
```