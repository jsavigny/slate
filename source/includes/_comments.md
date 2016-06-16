# Comments

## Get All Comments

> Sample Request

```ruby
GET /v1/comments
Host: apikomunitas.local.host:5000
```

```shell
curl "http://apikomunitas.local.host:5000/v1/comments"
```

> Sample Response


```json
{
  "status": "OK",
  "comments": [
    {
      "id": 4,
      "comment": "if i'm not back again this time tomorrow, carry on, **carry on**",
      "markeddown_comment": "<p>if i&rsquo;m not back again this time tomorrow, carry on, <strong>carry on</strong></p>\n",
      "short_id": "sbrlly",
      "created_at": "2016-06-13T14:40:59.000+07:00",
      "updated_at": "2016-06-13T14:40:59.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "parent_comment_id": 3,
      "user": {
        "username": "julio",
        "id": 1
      },
      "topic": {
        "title": "Mama, Just Killed a MAN",
        "id": 9
      }
    },
    {
      "id": 3,
      "comment": "Didn't mean to make you cry~",
      "markeddown_comment": "<p>Didn&rsquo;t mean to make you cry~</p>\n",
      "short_id": "ee6sgk",
      "created_at": "2016-06-13T14:35:59.000+07:00",
      "updated_at": "2016-06-13T14:35:59.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "parent_comment_id": 2,
      "user": {
        "username": "julio",
        "id": 1
      },
      "topic": {
        "title": "Mama, Just Killed a MAN",
        "id": 9
      }
    },
    {
      "id": 2,
      "comment": "Mamaaaa.... uuuuuu....",
      "markeddown_comment": "<p>Mamaaaa&hellip;. uuuuuu&hellip;.</p>\n",
      "short_id": "wdqric",
      "created_at": "2016-06-13T14:35:43.000+07:00",
      "updated_at": "2016-06-13T14:35:43.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "parent_comment_id": 1,
      "user": {
        "username": "julio",
        "id": 1
      },
      "topic": {
        "title": "Mama, Just Killed a MAN",
        "id": 9
      }
    },
    {
      "id": 1,
      "comment": "Pulled my trigger now he's dead!",
      "markeddown_comment": "<p>Pulled my trigger now he&rsquo;s dead!</p>\n",
      "short_id": "fpx9rg",
      "created_at": "2016-06-09T14:20:02.000+07:00",
      "updated_at": "2016-06-09T14:20:02.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "parent_comment_id": null,
      "user": {
        "username": "julio",
        "id": 1
      },
      "topic": {
        "title": "Mama, Just Killed a MAN",
        "id": 9
      }
    }
  ],
  "message": "Comments"
}
```


This endpoint retrieves all comments.

### HTTP Request

`GET http://apikomunitas.local.host/v1/comments `

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
`tag` | 'Semua' | The tag to filter the comments.
`page` | - | Pagination, each page will return 10 comments.