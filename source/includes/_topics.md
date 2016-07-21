# Topics

## Get All Topics

> Sample Request

```ruby
GET komunitas/topics?filter=recent&page=1&tag=Semua
Host: api.local.host:5000
```

```shell
curl "http://api.local.host:5000/komunitas/topics?filter=recent&page=1&tag=Semua"
```


> Sample Response

```json
{
  "status": "OK",
  "topics": [
    {
      "id": 71,
      "title": "Where is my mind?",
      "created_at": "2016-07-21T13:02:21.000+07:00",
      "updated_at": "2016-07-21T13:02:21.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": 1,
      "comments_count": 5,
      "is_sticky": false,
      "user": {
        "username": "jsavigny",
        "id": 1,
        "karma": 2
      },
      "tags": [
        {
          "tag": "Rileks",
          "description": "enjoy aja"
        }
      ]
    },
    {
      "id": 70,
      "title": "Ksong",
      "created_at": "2016-07-20T10:58:44.000+07:00",
      "updated_at": "2016-07-20T10:58:44.000+07:00",
      "upvotes": 2,
      "downvotes": 0,
      "vote": 1,
      "comments_count": 3,
      "is_sticky": false,
      "user": {
        "username": "rahmanadianto",
        "id": 3,
        "karma": 10
      },
      "tags": [
        {
          "tag": "Pengumuman",
          "description": "Hello, World!"
        }
      ]
    },
    {
      "id": 67,
      "title": "Ksong",
      "created_at": "2016-07-20T10:58:27.000+07:00",
      "updated_at": "2016-07-20T10:58:27.000+07:00",
      "upvotes": 2,
      "downvotes": 0,
      "vote": 1,
      "comments_count": 3,
      "is_sticky": false,
      "user": {
        "username": "rahmanadianto",
        "id": 3,
        "karma": 10
      },
      "tags": [
        {
          "tag": "Pengumuman",
          "description": "Hello, World!"
        }
      ]
    },
    {
      "id": 66,
      "title": "Ksong",
      "created_at": "2016-07-20T10:58:13.000+07:00",
      "updated_at": "2016-07-20T10:58:13.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": null,
      "comments_count": 3,
      "is_sticky": false,
      "user": {
        "username": "rahmanadianto",
        "id": 3,
        "karma": 10
      },
      "tags": [
        {
          "tag": "Pengumuman",
          "description": "Hello, World!"
        }
      ]
    },
    {
      "id": 65,
      "title": "Please",
      "created_at": "2016-07-19T19:47:03.000+07:00",
      "updated_at": "2016-07-19T19:47:03.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": null,
      "comments_count": 6,
      "is_sticky": false,
      "user": {
        "username": "rahmanadianto",
        "id": 3,
        "karma": 10
      },
      "tags": [
        {
          "tag": "Gadget",
          "description": "Inspect-her gadget!"
        }
      ]
    },
    {
      "id": 64,
      "title": "Topic ternary quh",
      "created_at": "2016-07-19T17:16:09.000+07:00",
      "updated_at": "2016-07-19T17:16:09.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": null,
      "comments_count": 10,
      "is_sticky": false,
      "user": {
        "username": "rahmanadianto",
        "id": 3,
        "karma": 10
      },
      "tags": [
        {
          "tag": "Rileks",
          "description": "enjoy aja"
        }
      ]
    },
    {
      "id": 63,
      "title": "Aaasdfasdf",
      "created_at": "2016-07-19T17:03:15.000+07:00",
      "updated_at": "2016-07-19T17:03:15.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": null,
      "comments_count": 6,
      "is_sticky": false,
      "user": {
        "username": "rahmanadianto",
        "id": 3,
        "karma": 10
      },
      "tags": [
        {
          "tag": "Pengumuman",
          "description": "Hello, World!"
        }
      ]
    },
    {
      "id": 62,
      "title": "Panjang",
      "created_at": "2016-07-15T11:14:45.000+07:00",
      "updated_at": "2016-07-15T11:14:45.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": null,
      "comments_count": 31,
      "is_sticky": false,
      "user": {
        "username": "rahmanadianto",
        "id": 3,
        "karma": 10
      },
      "tags": [
        {
          "tag": "Pengumuman",
          "description": "Hello, World!"
        }
      ]
    },
    {
      "id": 11,
      "title": "Topik 3",
      "created_at": "2016-06-29T10:54:32.000+07:00",
      "updated_at": "2016-06-29T10:56:48.000+07:00",
      "upvotes": 0,
      "downvotes": 0,
      "vote": null,
      "comments_count": 11,
      "is_sticky": true,
      "user": {
        "username": "jsavigny",
        "id": 1,
        "karma": 2
      },
      "tags": [
        {
          "tag": "Gadget",
          "description": "Inspect-her gadget!"
        }
      ]
    }
  ],
  "message": "Recent Topics"
}
```


This endpoint retrieves all topics, sticky and non sticky alike, sorted by trending or recency.

### HTTP Request

`GET http://api.local.host:5000/komunitas/topics `

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
`tag` | 'Semua' | The tag to filter the topics.
`filter` | - | If filter = recent,then the response will return topics sorted by recency (recent topics), else sorted by trending (trending topics)
`page` | - | Pagination, each page will return 8 topics

## Get a Specific Topic

> Sample Request

```ruby
GET komunitas/topics/1
Host: api.local.host:5000
```

```shell
curl "http://api.local.host:5000/komunitas/topics/1"
```

> Sample Response

```json
{
  "status": "OK",
  "topic": {
    "id": 71,
    "title": "Where is my mind?",
    "description": "With your feet on the air and your head on the ground.",
    "markeddown_description": "<p>With your feet on the air and your head on the ground.</p>\n",
    "created_at": "2016-07-21T13:02:21.000+07:00",
    "updated_at": "2016-07-21T13:02:21.000+07:00",
    "upvotes": 1,
    "downvotes": 0,
    "vote": 1,
    "comments_count": 6,
    "user": {
      "username": "jsavigny",
      "id": 1,
      "karma": 2
    },
    "tags": [
      {
        "tag": "Rileks",
        "description": "enjoy aja"
      }
    ]
  },
  "comments": [
    {
      "id": 199,
      "comment": "The first rule about..",
      "markeddown_comment": "<p>The first rule about..</p>\n",
      "created_at": "2016-07-21T14:53:31.000+07:00",
      "updated_at": "2016-07-21T14:53:31.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": null,
      "parent_comment_id": null,
      "user": {
        "username": "jsavigny",
        "id": 1,
        "karma": 2,
        "avatar": "http://www.local.host:5000/images/default_avatar/small/default.jpg"
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
      "parent_comment_id": null,
      "user": {
        "username": "jsavigny",
        "id": 1,
        "karma": 2,
        "avatar": "http://www.local.host:5000/images/default_avatar/small/default.jpg"
      }
    }
  ],
  "message": "Topic details"
}
```

> Not Found Response

```json
{
  "status": "ERROR",
  "message": "Not Found"
}
```

This endpoint retrieves a specific detailed topic, with its level 0 comments (comment that does not have parent).


### HTTP Request

`GET http://api.local.host:5000/komunitas/topics/:id`

### URL Parameters

Parameter | Description
--------- | -----------
`:id` | The ID of the topic to retrieve

## Create a topic

> Sample Request

```ruby
POST komunitas/topics
Host: api.local.host:5000
Authorization: Basic user_id:api_token
Content-Type Application/JSON
```

```json
{
  "topic":{
          "title":"Now I am become death",
          "tags_a":["Video","Gadget"],
          "description":"The destroyer of **THE WORLD**"
  }
}
```

```shell
curl -X POST "api.local.host:5000/komunitas/topics"
        -d  '{
              "topic":{
                      "title":"Now I am become death",
                      "tags_a":["Video","Gadget"],
                      "description":"The destroyer of **THE WORLD**"
              }
            }'
      -H "Content-Type: application/json"
      -u "1:RnLxZ69SP0tOmJoulmG7"
```
> Success Response

```json
{
  "status": "OK",
  "topic_detail": {
    "id": 8,
    "short_id": "y6msra",
    "title_as_url": "now_i_am_become_death"
  },
  "message": "Topic Created"
}
```

> No Parameter Error

```json
{
  "status": "ERROR",
  "message": "No Topic Parameter"
}
```

> Authentication Error

```json
{
  "status": "ERROR",
  "message": "Anda harus login untuk mengakses halaman ini"
}
```

This endpoint is used to create topic.
<aside class="notice"> Requires Authentication </aside>


### HTTP Request

`POST http://api.local.host:5000/komunitas/topics/`

### URL Parameters

Parameter |        |Description
--------- | -------- |-----------
`title` | required |Title of the topic
`tags_a` | required |Tags of the topic
`description` | required | Body/description of the topic

## Preview a topic

> Sample Request

```ruby
POST komunitas/topics/preview
Host: api.local.host:5000
Authorization: Basic user_id:api_token
Content-Type Application/JSON
```

```json
{
  "topic":{
          "title":"Now I am become death",
          "tags_a":["Video","Gadget"],
          "description":"The destroyer of **THE WORLD**"
  }
}
```

```shell
curl -X POST "api.local.host:5000/komunitas/topics"
        -d  '{
              "topic":{
                      "title":"Now I am become death",
                      "tags_a":["Video","Gadget"],
                      "description":"The destroyer of **THE WORLD**"
              }
            }'
      -H "Content-Type: application/json"
      -u "1:RnLxZ69SP0tOmJoulmG7"
```
> Success Response

```json
{
  "status": "OK",
  "topic_detail": {
    "title": "Now I am become death",
    "markeddown_description": "<p>The destroyer of <strong>THE WORLD</strong></p>\n"
  },
  "message": "Preview"
}
```

> No Parameter Error

```json
{
  "status": "ERROR",
  "message": "No Topic Parameter"
}
```

> Authentication Error

```json
{
  "status": "ERROR",
  "message": "Anda harus login untuk mengakses halaman ini"
}
```

This endpoint is used to preview a topic before creation.
<aside class="notice"> Requires Authentication </aside>


### HTTP Request

`POST http://api.local.host:5000/komunitas/topics/`

### URL Parameters

Parameter |        |Description
--------- | -------- |-----------
`title` | required |Title of the topic
`tags_a` | required |Tags of the topic
`description` | required | Body/description of the topic


## Upvote a topic

> Sample Request

```ruby
POST komunitas/topics/1/upvotes
Host: api.local.host:5000
Authorization: Basic user_id:api_token
```

```shell
curl -X POST "api.local.host:5000/komunitas/topics/1/upvotes"
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

This endpoint is used to upvote a topic.
<aside class="notice"> Requires Authentication </aside>


### HTTP Request

`POST http://api.local.host:5000/komunitas/topics/:id/upvotes`

### URL Parameters

Parameter |        |Description
--------- | -------- |-----------
`:id` | required |id of the topic

## Downvote a topic

> Sample Request

```ruby
POST komunitas/topics/1/downvotes
Host: api.local.host:5000
Authorization: Basic user_id:api_token
```

```json
{
  "reason":"O"
}
```

```shell
curl -X POST "api.local.host:5000/komunitas/topics/1/downvotes"
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

This endpoint is used to downvote a topic.
<aside class="notice"> Requires Authentication </aside>


### HTTP Request

`POST http://api.local.host:5000/komunitas/topics/:id/downvotes`

### URL Parameters

Parameter |        |Description
--------- | -------- |-----------
`:id` | required |id of the topic
`reason` | required | reason for the downvote
  |  | "O" => "Off-topic"
  |  | "A" => "Already Posted"
  |  | "T" => "Poorly Tagged"
  |  | "L" => "Poorly Titled"
  |  | "S" => "Spam"



## Unvote a topic

> Sample Request

```ruby
POST komunitas/topics/1/unvotes
Host: api.local.host:5000
Authorization: Basic user_id:api_token
```

```shell
curl -X POST "api.local.host:5000/komunitas/topics/1/unvotes"
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

This endpoint is used to unvote (remove vote from) a topic.
<aside class="notice"> Requires Authentication </aside>


### HTTP Request

`POST http://api.local.host:5000/komunitas/topics/:id/unvotes`

### URL Parameters

Parameter |        |Description
--------- | -------- |-----------
`:id` | required |id of the topic
