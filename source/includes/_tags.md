# Tags

## Get All Tags

> Sample Request

```ruby
GET komunitas/tags
Host: api.bukalapak.com
```

```shell
curl "http://api.bukalapak.com/komunitas/tags"
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

`GET http://api.local.host/komunitas/tags `
