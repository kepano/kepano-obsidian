# Recent entries

```dataview
table
	created as Date
where
	contains(file.outlinks, this.file.link)
sort created desc
limit 20
```