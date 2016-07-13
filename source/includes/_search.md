# Search

## Search topics/comments

> Sample Request

```ruby
GET komunitas/v1/search?forum_search[q]=tes&forum_search[what]=all
Host: api.local.host:5000
```

```shell
curl "http://api.local.host:5000/komunitas/v1/search?forum_search[q]=tes&forum_search[what]=all"
```

> Sample Response


```json
{
  "status": "OK",
  "topics": [
    {
      "id": 12,
      "title": "Topik 4",
      "created_at": "2016-06-29T10:54:44.000+07:00",
      "updated_at": "2016-06-29T10:54:44.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "comments_count": 1,
      "user": {
        "username": "jsavigny",
        "id": 1,
        "karma": 1
      },
      "tags": [
        {
          "tag": "Kamera",
          "description": "Double tap to love"
        }
      ]
    },
    {
      "id": 14,
      "title": "Topik 6",
      "created_at": "2016-06-30T10:11:26.000+07:00",
      "updated_at": "2016-06-30T10:11:26.000+07:00",
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
          "tag": "Sepeda",
          "description": "I want to ride my bicycle~"
        }
      ]
    },
    {
      "id": 58,
      "title": "Ini bergambar loh",
      "created_at": "2016-07-12T19:06:21.000+07:00",
      "updated_at": "2016-07-12T19:06:21.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "comments_count": 0,
      "user": {
        "username": "juliosavigny",
        "id": 2,
        "karma": 0
      },
      "tags": [
        {
          "tag": "Kamera",
          "description": "Double tap to love"
        }
      ]
    },
    {
      "id": 46,
      "title": "Once upon a time, I dreamt I was a butterfly",
      "created_at": "2016-07-01T08:12:53.000+07:00",
      "updated_at": "2016-07-01T08:12:53.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "comments_count": 3,
      "user": {
        "username": "jsavigny",
        "id": 1,
        "karma": 1
      },
      "tags": [
        {
          "tag": "Rileks",
          "description": "enjoy aja"
        }
      ]
    }
  ],
  "comments": [
    {
      "id": 8,
      "comment": "Yoi",
      "markeddown_comment": "<p>Yoi</p>\n",
      "created_at": "2016-06-30T11:04:38.000+07:00",
      "updated_at": "2016-06-30T11:04:38.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "user": {
        "username": "jsavigny",
        "id": 1,
        "karma": 1
      },
      "topic": {
        "title": "Topik 7",
        "id": 15
      }
    },
    {
      "id": 18,
      "comment": "oh iya ya? okedeh",
      "markeddown_comment": "<p>oh iya ya? okedeh</p>\n",
      "created_at": "2016-07-01T08:47:51.000+07:00",
      "updated_at": "2016-07-01T08:47:51.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "user": {
        "username": "jsavigny",
        "id": 1,
        "karma": 1
      },
      "topic": {
        "title": "Once upon a time, I dreamt I was a butterfly",
        "id": 46
      }
    },
    {
      "id": 17,
      "comment": "Now I do not know whether I was then a man dreaming I was a butterfly, or whether I am now a butterfly, dreaming I am a man.",
      "markeddown_comment": "<p>Now I do not know whether I was then a man dreaming I was a butterfly, or whether I am now a butterfly, dreaming I am a man.</p>\n",
      "created_at": "2016-07-01T08:13:13.000+07:00",
      "updated_at": "2016-07-01T08:13:13.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "user": {
        "username": "jsavigny",
        "id": 1,
        "karma": 1
      },
      "topic": {
        "title": "Once upon a time, I dreamt I was a butterfly",
        "id": 46
      }
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
