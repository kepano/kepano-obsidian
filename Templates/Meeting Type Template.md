#meetings/type 

```dataview
table without id file.link as Meeting, people as People, date as Date
from #meetings or #dates
where !contains(file.name,"Template") and contains(type,this.file.link)
sort date desc
limit 50
```