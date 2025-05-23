Analysis of cost per use, see [[Buy wisely]]

```dataview
table without id
	file.link as Product,
	rating as Rating,
	"$" + round(price/(monthly-uses*((date(today) - acquired).months)),2) as "Per use",
	monthly-uses as "Uses/month",
	dateformat(acquired, "yyyy-MM") as Acquired,
	round((date(today) - acquired).months,1) as "Months",
	"$" + string(round(price, 2)) as Price,
	round(monthly-uses*((date(today) - acquired).months),0) as "Total uses",
	type as Type
where
	monthly-uses > 0 and
	contains(categories, [[Products]])
sort
	round(price/(monthly-uses*((date(today) - acquired).months)),2) asc
```