#music/genres

```dataview
table without id file.link as Album, artist as "Artist", genre as "Genre", rating as "Rating"
from #albums
where genre = this.file.link or contains(genre,this.file.link)
sort rating desc
```