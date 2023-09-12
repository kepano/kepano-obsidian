## Favorites

```dataview
table without id file.link as Book, author as Author, year as Year, rating as Rating, created as Added, last as "Last read", genre as Genre
from #books 
where !contains(file.name, "Template") and rating > 5
sort rating desc, date asc
limit 100
```
