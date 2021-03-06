Paths API
============
The paths API allows you to index all paths contained in a nation and returns the path ID and path steps that are associated with that path.

Index Endpoint
--------------
The index endpoint provides a paginated list of the paths in a nation.
```
GET /api/v1/paths
```
### Parameters
* `limit` - max number of results to show in one page of results (default 10, max 100).
* `__nonce` - generated pagination nonce. Do not modify.
* `__token` - generated pagination token. Do not modify.

### Example
If you make a request like this:
```
GET https://foobar.nationbuilder.com/api/v1/paths
```

Then you should get a 200 response with a body like this:
```json
{
      "id": 8,
      "name": "Become a donor",
      "created_at": "2016-03-15T14:47:22-07:00",
      "updated_at": "2016-03-15T14:47:22-07:00",
      "path_steps": [     
        {
          "name": "Ask to pledge",
          "position": "2",
          "created_at": "2016-03-15T14:47:22-07:00",
          "updated_at": "2016-03-15T14:47:22-07:00"
        },
        {
          "name": "Ask to donate",
          "position": "4",
          "created_at": "2016-03-15T14:47:22-07:00",
          "updated_at": "2016-03-15T14:47:22-07:00"
        },
        {
          "name": "Donated",
          "position": "5",
          "created_at": "2016-03-15T14:47:22-07:00",
          "updated_at": "2016-03-15T14:47:22-07:00"
        }
      ]
    },
{
      "id": 10,
      "name": "Become a paid member",
      "created_at": "2016-03-15T14:47:22-07:00",
      "updated_at": "2016-03-15T14:47:22-07:00",
      "path_steps": [
        {
          "name": "Potential member",
          "position": "1",
          "created_at": "2016-03-15T14:47:22-07:00",
          "updated_at": "2016-03-15T14:47:22-07:00"
        },
        {
          "name": "Send membership invite",
          "position": "2",
          "created_at": "2016-03-15T14:47:22-07:00",
          "updated_at": "2016-03-15T14:47:22-07:00"
        },
        {
          "name": "Paid for membership",
          "position": "4",
          "created_at": "2016-03-15T14:47:22-07:00",
          "updated_at": "2016-03-15T14:47:22-07:00"
        }
      ]
    }
  ],
  "next": "/api/v1/paths?__nonce=LfvJrP4Lb3zJKmS4T-YRwQ\u0026__token=APFuGgDsV9ZuyIuycHOdr_gZxJX6_gBcGOS53AHVl0si",
  "prev": null
}
```
