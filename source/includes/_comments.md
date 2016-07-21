# Comments

## Get All Comments

> Sample Request

```ruby
GET komunitas/comments
Host: api.local.host:5000
```

```shell
curl "http://api.local.host:5000/komunitas/comments"
```

> Sample Response


```json
{
  "status": "OK",
  "comments": [
    {
      "id": 199,
      "comment": "The first rule about..",
      "markeddown_comment": "<p>The first rule about..</p>\n",
      "created_at": "2016-07-21T14:53:31.000+07:00",
      "updated_at": "2016-07-21T14:53:31.000+07:00",
      "upvotes": 0,
      "downvotes": 0,
      "vote": null,
      "user": {
        "username": "jsavigny",
        "id": 1,
        "karma": 2,
        "avatar": "http://www.local.host:5000/images/default_avatar/small/default.jpg"
      },
      "topic": {
        "title": "Where is my mind?",
        "id": 71
      }
    },
    {
      "id": 198,
      "comment": "Whe~re is my mind?...",
      "markeddown_comment": "<p>Whe~re is my mind?&hellip;</p>\n",
      "created_at": "2016-07-21T13:03:14.000+07:00",
      "updated_at": "2016-07-21T13:03:14.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": 1,
      "user": {
        "username": "jsavigny",
        "id": 1,
        "karma": 2,
        "avatar": "http://www.local.host:5000/images/default_avatar/small/default.jpg"
      },
      "topic": {
        "title": "Where is my mind?",
        "id": 71
      }
    },
    {
      "id": 197,
      "comment": "Where is my mind?",
      "markeddown_comment": "<p>Where is my mind?</p>\n",
      "created_at": "2016-07-21T13:03:02.000+07:00",
      "updated_at": "2016-07-21T13:03:02.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": 1,
      "user": {
        "username": "jsavigny",
        "id": 1,
        "karma": 2,
        "avatar": "http://www.local.host:5000/images/default_avatar/small/default.jpg"
      },
      "topic": {
        "title": "Where is my mind?",
        "id": 71
      }
    },
    {
      "id": 196,
      "comment": "Where is my mind?",
      "markeddown_comment": "<p>Where is my mind?</p>\n",
      "created_at": "2016-07-21T13:02:57.000+07:00",
      "updated_at": "2016-07-21T13:02:57.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": 1,
      "user": {
        "username": "jsavigny",
        "id": 1,
        "karma": 2,
        "avatar": "http://www.local.host:5000/images/default_avatar/small/default.jpg"
      },
      "topic": {
        "title": "Where is my mind?",
        "id": 71
      }
    },
    {
      "id": 195,
      "comment": "Your head will collapse, \r\nbut there's nothing in it and you ask yourselves.",
      "markeddown_comment": "<p>Your head will collapse,</p>\n\n<p>but there&rsquo;s nothing in it and you ask yourselves.</p>\n",
      "created_at": "2016-07-21T13:02:50.000+07:00",
      "updated_at": "2016-07-21T13:02:50.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": 1,
      "user": {
        "username": "jsavigny",
        "id": 1,
        "karma": 2,
        "avatar": "http://www.local.host:5000/images/default_avatar/small/default.jpg"
      },
      "topic": {
        "title": "Where is my mind?",
        "id": 71
      }
    },
    {
      "id": 194,
      "comment": "Try this trick, and spin it. Yeah!",
      "markeddown_comment": "<p>Try this trick, and spin it. Yeah!</p>\n",
      "created_at": "2016-07-21T13:02:31.000+07:00",
      "updated_at": "2016-07-21T13:02:31.000+07:00",
      "upvotes": 0,
      "downvotes": 0,
      "vote": null,
      "user": {
        "username": "jsavigny",
        "id": 1,
        "karma": 2,
        "avatar": "http://www.local.host:5000/images/default_avatar/small/default.jpg"
      },
      "topic": {
        "title": "Where is my mind?",
        "id": 71
      }
    },
    {
      "id": 193,
      "comment": "op siiih",
      "markeddown_comment": "<p>op siiih</p>\n",
      "created_at": "2016-07-20T18:54:32.000+07:00",
      "updated_at": "2016-07-20T18:54:32.000+07:00",
      "upvotes": 2,
      "downvotes": 0,
      "vote": 1,
      "user": {
        "username": "juliosavigny",
        "id": 2,
        "karma": 2,
        "avatar": "http://www.local.host:5000/system4/avatars/1/small/250px-Stannis_sigil_coat.png"
      },
      "topic": {
        "title": "Ksong",
        "id": 69
      }
    },
    {
      "id": 192,
      "comment": "hai",
      "markeddown_comment": "<p>hai</p>\n",
      "created_at": "2016-07-20T18:53:57.000+07:00",
      "updated_at": "2016-07-20T18:53:57.000+07:00",
      "upvotes": 2,
      "downvotes": 0,
      "vote": 1,
      "user": {
        "username": "juliosavigny",
        "id": 2,
        "karma": 2,
        "avatar": "http://www.local.host:5000/system4/avatars/1/small/250px-Stannis_sigil_coat.png"
      },
      "topic": {
        "title": "Aaa",
        "id": 60
      }
    }
  ],
  "message": "Comments"
}

```


This endpoint retrieves all comments.

### HTTP Request

`GET http://api.local.host/komunitas/comments `

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
`tag` | 'Semua' | The tag to filter the comments.
`page` | - | Pagination, each page will return 8 comments.

## Get a Specific Comment

> Sample Request

```ruby
GET komunitas/comments/16
Host: api.local.host:5000
```

```shell
curl "http://api.local.host:5000/komunitas/comments/16"
```

> Sample Response

```json
{
  "status": "OK",
  "comment": {
    "id": 194,
    "comment": "Try this trick, and spin it. Yeah!",
    "markeddown_comment": "<p>Try this trick, and spin it. Yeah!</p>\n",
    "created_at": "2016-07-21T13:02:31.000+07:00",
    "updated_at": "2016-07-21T13:02:31.000+07:00",
    "upvotes": 0,
    "downvotes": 0,
    "vote": null,
    "parent_comment_id": null,
    "user": {
      "username": "jsavigny",
      "id": 1,
      "karma": 2,
      "avatar": "http://www.local.host:5000/images/default_avatar/small/default.jpg"
    },
    "topic": {
      "title": "Where is my mind?",
      "id": 71
    }
  },
  "child_comments": [
    {
      "id": 195,
      "comment": "Your head will collapse, \r\nbut there's nothing in it and you ask yourselves.",
      "markeddown_comment": "<p>Your head will collapse,</p>\n\n<p>but there&rsquo;s nothing in it and you ask yourselves.</p>\n",
      "created_at": "2016-07-21T13:02:50.000+07:00",
      "updated_at": "2016-07-21T13:02:50.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": 1,
      "parent_comment_id": 194,
      "user": {
        "username": "jsavigny",
        "id": 1,
        "karma": 2,
        "avatar": "http://www.local.host:5000/images/default_avatar/small/default.jpg"
      }
    },
    {
      "id": 196,
      "comment": "Where is my mind?",
      "markeddown_comment": "<p>Where is my mind?</p>\n",
      "created_at": "2016-07-21T13:02:57.000+07:00",
      "updated_at": "2016-07-21T13:02:57.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": 1,
      "parent_comment_id": 195,
      "user": {
        "username": "jsavigny",
        "id": 1,
        "karma": 2,
        "avatar": "http://www.local.host:5000/images/default_avatar/small/default.jpg"
      }
    },
    {
      "id": 197,
      "comment": "Where is my mind?",
      "markeddown_comment": "<p>Where is my mind?</p>\n",
      "created_at": "2016-07-21T13:03:02.000+07:00",
      "updated_at": "2016-07-21T13:03:02.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": 1,
      "parent_comment_id": 196,
      "user": {
        "username": "jsavigny",
        "id": 1,
        "karma": 2,
        "avatar": "http://www.local.host:5000/images/default_avatar/small/default.jpg"
      }
    },
    {
      "id": 198,
      "comment": "Whe~re is my mind?...",
      "markeddown_comment": "<p>Whe~re is my mind?&hellip;</p>\n",
      "created_at": "2016-07-21T13:03:14.000+07:00",
      "updated_at": "2016-07-21T13:03:14.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": 1,
      "parent_comment_id": 197,
      "user": {
        "username": "jsavigny",
        "id": 1,
        "karma": 2,
        "avatar": "http://www.local.host:5000/images/default_avatar/small/default.jpg"
      }
    }
  ],
  "message": "Comment details"
}
```

> Not Found Response

```json
{
  "status": "ERROR",
  "message": "Not Found"
}
```

This endpoint retrieves a specific detailed comments, with its child comments (if exist).


### HTTP Request

`GET http://api.local.host:5000/komunitas/comments/:id`

### URL Parameters

Parameter | Description
--------- | -----------
`:id` | The ID of the comment to retrieve

## Create a comment

> Sample Request

```ruby
POST komunitas/comments
Host: api.local.host:5000
Authorization: Basic user_id:api_token
Content-Type Application/JSON
```

```json
{
    "comment":"What?",
    "story_id":1
}
```

```shell
curl -X POST "api.local.host:5000/komunitas/topics"
        -d  '{
                "comment":"What?",
                "story_id":1
             }'
      -H "Content-Type: application/json"
      -u "1:RnLxZ69SP0tOmJoulmG7"
```


> Success Response

```json
{
  "status": "OK",
  "comment": {
    "id": 19,
    "story_id": 1,
    "parent_comment_id": null
  },
  "message": "Comment created"
}
```

> Sample Request (with parent comment)

```json
{
    "comment":"What?",
    "story_id":1,
    "parent_comment_id":24

}
```

```shell
curl -X POST "api.local.host:5000/komunitas/topics"
        -d  '{
                "comment":"What?",
                "story_id":1,
                "parent_comment_id":24
             }'
      -H "Content-Type: application/json"
      -u "1:RnLxZ69SP0tOmJoulmG7"
```

> Success Response

```json
{
  "status": "OK",
  "comment": {
    "id": 25,
    "story_id": 1,
    "parent_comment_id": 24
  },
  "message": "Comment created"
}
```
> Story Not Found Error response

```json
{
  "status": "ERROR",
  "message": "Story Not Found"
}
```
> Invalid Parent Comment Error response

```json
{
  "status": "ERROR",
  "message": "Invalid Parent Comment"
}
```
> Recently commented here Error response

```json
{
  "status": "ERROR",
  "message": "You have already posted a comment here recently."
}
```

> Authentication Error response

```json
{
  "status": "ERROR",
  "message": "Anda harus login untuk mengakses halaman ini"
}
```

This endpoint is used to create a comment, either by commenting a topic, or by replying another comment
<aside class="notice"> Requires Authentication </aside>


### HTTP Request

`POST http://api.local.host:5000/komunitas/comments/`

### URL Parameters

Parameter |        |Description
--------- | ------------ |-----------
`comment` | required |The comment
`story_id` | required | id of the story that you're commenting
`parent_comment_id` | not required | id of the comment that you're replying to


## Upvote a comment

> Sample Request

```ruby
POST komunitas/comments/1/upvotes
Host: api.local.host:5000
Authorization: Basic user_id:api_token
```

```shell
curl -X POST "api.local.host:5000/komunitas/comments/1/upvotes"
      -u "1:RnLxZ69SP0tOmJoulmG7"
```
> Success Response

```json
{
  "status": "OK",
  "message": "Upvote Success"
}
```

> Authentication Error

```json
{
  "status": "ERROR",
  "message": "Anda harus login untuk mengakses halaman ini"
}
```

This endpoint is used to upvote a comment.
<aside class="notice"> Requires Authentication </aside>


### HTTP Request

`POST http://api.local.host:5000/komunitas/comments/:id/upvotes`

### URL Parameters

Parameter |        |Description
--------- | -------- |-----------
`:id` | required |id of the comment

## Downvote a comment

> Sample Request

```ruby
POST komunitas/comments/1/downvotes
Host: api.local.host:5000
Authorization: Basic user_id:api_token
```

```json
{
  "reason":"O"
}
```

```shell
curl -X POST "api.local.host:5000/komunitas/comments/1/downvotes"
      -d '{ "reason":"O" }'
      -u "1:RnLxZ69SP0tOmJoulmG7"
```
> Success Response

```json
{
  "status": "OK",
  "message": "Downvote Success"
}
```

> Authentication Error

```json
{
  "status": "ERROR",
  "message": "Anda harus login untuk mengakses halaman ini"
}
```

> Invalid Reason

```json
{
  "status": "ERROR",
  "message": "Invalid Reason"
}
```

> Not Permitted

```json
{
  "status": "ERROR",
  "message": "Not Permitted to Downvote"
}
```

This endpoint is used to downvote a comment.
<aside class="notice"> Requires Authentication </aside>


### HTTP Request

`POST http://api.local.host:5000/komunitas/comments/:id/downvotes`

### URL Parameters

Parameter |        |Description
--------- | -------- |-----------
`:id` | required |id of the comment
`reason` | required | reason for the downvote
 | | "O" => "Off-topic"
 | | "I" => "Incorrect"
 | | "M" => "Me-too"
 | | "T" => "Troll"
 | | "S" => "Spam"



## Unvote a comment

> Sample Request

```ruby
POST komunitas/comments/1/unvotes
Host: api.local.host:5000
Authorization: Basic user_id:api_token
```

```shell
curl -X POST "api.local.host:5000/komunitas/comments/1/unvotes"
      -u "1:RnLxZ69SP0tOmJoulmG7"
```
> Success Response

```json
{
  "status": "OK",
  "message": "Unvote Success"
}
```

> Authentication Error

```json
{
  "status": "ERROR",
  "message": "Anda harus login untuk mengakses halaman ini"
}
```

This endpoint is used to unvote (remove vote from) a comment.
<aside class="notice"> Requires Authentication </aside>


### HTTP Request

`POST http://api.local.host:5000/komunitas/comments/:id/unvotes`

### URL Parameters

Parameter |        |Description
--------- | -------- |-----------
`:id` | required |id of the comment
