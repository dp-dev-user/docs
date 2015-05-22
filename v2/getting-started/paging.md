Paging
======
Every query that doesn't result in a single resource consists of the following properties.


``` js
{
	"result": [
		... // Contains the list of results from the query
	],
	"totalResult": <total numer of hits>,
	"previous": <absolute link to previous page>,
	"next": <absolute link to next page>
}
```

The result can be paged by following the previous and next links or paged by providing special paging parameters.

- **start** how many items to skip (defaults to 0)
- **pageSize** how many items you want in the response (defaults to 25)

example:

> /drinks/?start=100&pageSize=30


Continue reading about [authentication](/drinks-api/docs/v2/getting-started/authentication)