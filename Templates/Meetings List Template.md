```dataview
table without id
	file.link as Meeting, date as Date
from [[Meetings]]
where contains(people,this.file.link)
sort date desc
limit 50
```