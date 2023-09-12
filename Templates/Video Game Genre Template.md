#games/genres

```dataview
table maker as "Maker", year as "Year", rating as "Rating"
from #games
where !contains(file.name, "Template") and contains(genre, this.file.link)
sort rating desc
```