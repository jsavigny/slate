# Tags

## Get All Tags

> Sample Request

```ruby
GET komunitas/v1/tags
Host: api.local.host:5000
```

```shell
curl "http://api.local.host:5000/komunitas/v1/tags"
```

> Sample Response


```json
{
  "status": "OK",
  "tags": [
    {
      "key": 1,
      "tag": "Test",
      "description": "Test"
    },
    {
      "key": 2,
      "tag": "Test2",
      "description": "Test2x"
    }
  ],
  "message": "Tags"
}
```


This endpoint retrieves all tags.

### HTTP Request

`GET http://api.local.host/komunitas/v1/tags `
