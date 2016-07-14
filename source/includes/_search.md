# Search

## Search topics/comments

> Sample Request

```ruby
GET komunitas/v1/search?forum_search[q]=tes&forum_search[what]=all
Host: api.local.host:5000
```

```shell
curl "http://api.local.host:5000/komunitas/v1/search?forum_search[q]=death&forum_search[what]=all&page=1"
```

> Sample Response


```json
{
  "status": "OK",
  "topics": [
    {
      "id": 45,
      "title": "Now I am become death",
      "created_at": "2016-07-01T08:08:35.000+07:00",
      "updated_at": "2016-07-01T08:08:35.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "comments_count": 1,
      "user": {
        "username": "rahmanadianto",
        "id": 3,
        "karma": 0
      },
      "tags": [
        {
          "tag": "Video",
          "description": "Bukan XXX"
        },
        {
          "tag": "Gadget",
          "description": "Inspect-her gadget!"
        }
      ]
    },
    {
      "id": 59,
      "title": "Now I am become death",
      "created_at": "2016-07-12T19:20:23.000+07:00",
      "updated_at": "2016-07-12T19:20:23.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "comments_count": 0,
      "user": {
        "username": "rahmanadianto",
        "id": 3,
        "karma": 0
      },
      "tags": [
        {
          "tag": "Video",
          "description": "Bukan XXX"
        },
        {
          "tag": "Gadget",
          "description": "Inspect-her gadget!"
        }
      ]
    },
    {
      "id": 49,
      "title": "Now I am become death",
      "created_at": "2016-07-12T17:32:45.000+07:00",
      "updated_at": "2016-07-12T17:32:45.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "comments_count": 0,
      "user": {
        "username": "rahmanadianto",
        "id": 3,
        "karma": 0
      },
      "tags": [
        {
          "tag": "Video",
          "description": "Bukan XXX"
        },
        {
          "tag": "Gadget",
          "description": "Inspect-her gadget!"
        }
      ]
    },
    {
      "id": 44,
      "title": "Yeaaah",
      "created_at": "2016-06-30T14:41:34.000+07:00",
      "updated_at": "2016-06-30T14:43:38.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "comments_count": 0,
      "user": {
        "username": "jsavigny",
        "id": 1,
        "karma": 1
      },
      "tags": [
        {
          "tag": "Video",
          "description": "Bukan XXX"
        }
      ]
    }
  ],
  "message": "Search"
}
```


This endpoint retrieves topics/comments from a search query.

### HTTP Request

`GET http://api.local.host/komunitas/v1/search `

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
`forum_search[q]` | - | Search query
`forum_search[what]` | - | Option
 |  | "story" => Search topics
 |  | "comment" => Search comments
 |  | "all" => Search both topics and comments
`page` | - | Pagination, each page will return 20 combination of topics and comments
