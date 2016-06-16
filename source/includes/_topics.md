# Topics

## Get All Topics

> Sample Request

```ruby
GET /v1/topics?filter=recent?page=1
Host: apikomunitas.local.host:5000
```

```shell
curl "http://apikomunitas.local.host:5000/v1/topics?filter=recent"
```


> Sample Response

```json
{
  "status": "OK",
  "topics": [
    {
      "id": 43,
      "short_id": "q1uj1y",
      "title": "Now I am become death",
      "created_at": "2016-06-13T10:54:35.000+07:00",
      "updated_at": "2016-06-13T10:54:35.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "comments_count": 0,
      "user": {
        "username": "julio",
        "id": 1
      },
      "tags": [
        {
          "name": "Test",
          "description": "Test"
        }
      ]
    },
    {
      "id": 42,
      "short_id": "u9mcgd",
      "title": "Mama, Just Killed a MAN 2 Tag",
      "created_at": "2016-06-13T10:46:08.000+07:00",
      "updated_at": "2016-06-13T10:46:08.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "comments_count": 0,
      "user": {
        "username": "julio",
        "id": 1
      },
      "tags": [
        {
          "name": "Test",
          "description": "Test"
        }
      ]
    },
    {
      "id": 41,
      "short_id": "enam71",
      "title": "inocchi",
      "created_at": "2016-06-10T12:01:18.000+07:00",
      "updated_at": "2016-06-10T12:01:18.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "comments_count": 0,
      "user": {
        "username": "julio",
        "id": 1
      },
      "tags": [
        {
          "name": "Test",
          "description": "Test"
        }
      ]
    }
  ],
  "message": "Recent Topics"
}
```


This endpoint retrieves all topics, sorted by trending or recency.

### HTTP Request

`GET http://apikomunitas.local.host/v1/topics `

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
`tag` | 'Semua' | The tag to filter the topics.
`filter` | - | If filter = recent,then the response will return topics sorted by recency (recent topics), else sorted by trending (trending topics)
`page` | - | Pagination, each page will return 10 topics

## Get a Specific Topic

> Sample Request

```ruby
GET /v1/topics/9
Host: apikomunitas.local.host:5000
```

```shell
curl "http://apikomunitas.local.host:5000/v1/topics/9"
```

> Sample Response

```json
{
  "status": "OK",
  "topic": {
    "id": 9,
    "short_id": "36fu9q",
    "title": "Mama, Just Killed a MAN",
    "description": "Put a **GUN** against his head",
    "markeddown_description": "<p>Put a <strong>GUN</strong> against his head</p>\n",
    "created_at": "2016-06-09T12:51:14.000+07:00",
    "updated_at": "2016-06-09T12:51:14.000+07:00",
    "upvotes": 1,
    "downvotes": 0,
    "comments_count": 4,
    "user": {
      "username": "julio",
      "id": 1
    },
    "tags": [
      {
        "name": "Test",
        "description": "Test"
      }
    ]
  },
  "comments": [
    {
      "id": 1,
      "short_id": "fpx9rg",
      "comment": "Pulled my trigger now he's dead!",
      "markeddown_comment": "<p>Pulled my trigger now he&rsquo;s dead!</p>\n",
      "created_at": "2016-06-09T14:20:02.000+07:00",
      "updated_at": "2016-06-09T14:20:02.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "user": {
        "username": "julio",
        "id": 1
      }
    },
    {
      "id": 2,
      "short_id": "wdqric",
      "comment": "Mamaaaa.... uuuuuu....",
      "markeddown_comment": "<p>Mamaaaa&hellip;. uuuuuu&hellip;.</p>\n",
      "created_at": "2016-06-13T14:35:43.000+07:00",
      "updated_at": "2016-06-13T14:35:43.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "user": {
        "username": "julio",
        "id": 1
      }
    },
    {
      "id": 3,
      "short_id": "ee6sgk",
      "comment": "Didn't mean to make you cry~",
      "markeddown_comment": "<p>Didn&rsquo;t mean to make you cry~</p>\n",
      "created_at": "2016-06-13T14:35:59.000+07:00",
      "updated_at": "2016-06-13T14:35:59.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "user": {
        "username": "julio",
        "id": 1
      }
    },
    {
      "id": 4,
      "short_id": "sbrlly",
      "comment": "if i'm not back again this time tomorrow, carry on, **carry on**",
      "markeddown_comment": "<p>if i&rsquo;m not back again this time tomorrow, carry on, <strong>carry on</strong></p>\n",
      "created_at": "2016-06-13T14:40:59.000+07:00",
      "updated_at": "2016-06-13T14:40:59.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "user": {
        "username": "julio",
        "id": 1
      }
    }
  ],
  "message": "Topic details"
}
```

This endpoint retrieves a specific detailed topic, with its comments (if exist).


### HTTP Request

`GET http://apikomunitas.local.host:5000/v1/topics/:id`

### URL Parameters

Parameter | Description
--------- | -----------
`:id` | The ID of the topic to retrieve

## Create a topic

> Sample Request

```ruby
POST /v1/topics
Host: apikomunitas.local.host:5000
Authorization: Basic user_id:api_token
```

```json
{
  "topic":{
          "title":"Now I am become death",
          "tags_a":["Test","zxc"],
          "description":"The destroyer of **THE WORLD**"
  }
}
```

```shell
curl -X POST "apikomunitas.local.host:5000/v1/topics"
        -d  '{
              "topic":{
                      "title":"Now I am become death",
                      "tags_a":["Test","zxc"],
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
    "id": 43,
    "short_id": "q1uj1y",
    "title_as_url": "now_i_am_become_death"
  },
  "message": "Topic Created"
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

`POST http://apikomunitas.local.host:5000/v1/topics/`

### URL Parameters

Parameter |        |Description
--------- | -------- |-----------
`title` | required |Title of the topic
`tags_a` | required |Tags of the topic
`description` | required | Body/description of the topic

## Upvote a topic

> Sample Request

```ruby
POST /v1/topics/1/upvotes
Host: apikomunitas.local.host:5000
Authorization: Basic user_id:api_token
```

```shell
curl -X POST "apikomunitas.local.host:5000/v1/topics/1/upvotes"
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

`POST http://apikomunitas.local.host:5000/v1/topics/:id/upvotes`

### URL Parameters

Parameter |        |Description
--------- | -------- |-----------
`:id` | required |id of the topic

## Downvote a topic

> Sample Request

```ruby
POST /v1/topics/1/downvotes
Host: apikomunitas.local.host:5000
Authorization: Basic user_id:api_token
```

```json
{
  "reason":"O"
}
```

```shell
curl -X POST "apikomunitas.local.host:5000/v1/topics/1/downvotes"
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

`POST http://apikomunitas.local.host:5000/v1/topics/:id/downvotes`

### URL Parameters

Parameter |        |Description
--------- | -------- |-----------
`:id` | required |id of the topic
`reason` | required | reason for the downvote
 | | "O" => "Off-topic",
 | | "I" => "Incorrect",
 | | "M" => "Me-too",
 | | "T" => "Troll",
 | | "S" => "Spam",



## Unvote a topic

> Sample Request

```ruby
POST /v1/topics/1/unvotes
Host: apikomunitas.local.host:5000
Authorization: Basic user_id:api_token
```

```shell
curl -X POST "apikomunitas.local.host:5000/v1/topics/1/unvotes"
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

`POST http://apikomunitas.local.host:5000/v1/topics/:id/unvotes`

### URL Parameters

Parameter |        |Description
--------- | -------- |-----------
`:id` | required |id of the topic