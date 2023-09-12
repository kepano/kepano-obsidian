## Favorites

```dataview
table without id file.link as Movie, year as "Year", ratingImdb as "Rating", last as "Last seen", director as "Director"
from #movies
where rating > 9
sort rating desc
```

## Last seen

```dataview
table without id file.link as Movie, year as "Year", rating as "Rating", last as "Last seen", director as "Director"
from #movies
where last != "" and !contains(file.name, "Template")
sort last desc
limit 100
```