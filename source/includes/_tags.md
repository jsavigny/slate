# Tags

## Get All Tags

> Sample Request

```ruby
POST /v1/tags
Host: apikomunitas.local.host:5000
```

```shell
curl "http://apikomunitas.local.host:5000/v1/tags"
```

> Sample Response


```json
{
  "status": "OK",
  "tags": [
    {
      "tag": "Test",
      "description": "Test"
    },
    {
      "tag": "Test2",
      "description": "Test2x"
    }
  ],
  "message": "Tags"
}
```


This endpoint retrieves all tags.

### HTTP Request

`GET http://apikomunitas.local.host/v1/tags `