
```dataview
list 
where
	contains(type, this.file.link) and
	!contains(file.name, "Template")
sort file.ctime asc
```