# Topics

## Get All Topics

> Sample Request

```ruby
GET komunitas/v1/topics?filter=recent&page=1&tag=Semua
Host: api.local.host:5000
```

```shell
curl "http://api.local.host:5000/komunitas/v1/topics?filter=recent&page=1&tag=Semua"
```


> Sample Response

```json
{
  "status": "OK",
  "topics": [
    {
      "id": 1,
      "short_id": "ez0iyc",
      "title": "Now I am become death",
      "created_at": "2016-06-15T19:35:14.000+07:00",
      "updated_at": "2016-06-15T19:35:14.000+07:00",
      "upvotes": 2,
      "downvotes": 0,
      "comments_count": 0,
      "user": {
        "username": "jsavigny",
        "id": 1,
        "karma": 4
      },
      "tags": [
        {
          "name": "Video",
          "description": "Video"
        }
      ]
    },
    {
      "id": 4,
      "short_id": "jwhhum",
      "title": "Ryu ga waga",
      "created_at": "2016-06-17T10:44:35.000+07:00",
      "updated_at": "2016-06-17T10:44:35.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "comments_count": 0,
      "user": {
        "username": "jsavigny",
        "id": 1,
        "karma": 4
      },
      "tags": [
        {
          "name": "Video",
          "description": "Video"
        }
      ]
    }
  ],
  "sticky_topics": [   
    {
      "id": 3,
      "short_id": "zxn9vq",
      "title": "This is a sticky story, which is very important",
      "created_at": "2016-06-15T19:35:14.000+07:00",
      "updated_at": "2016-06-15T19:35:14.000+07:00",
      "upvotes": 10,
      "downvotes": 0,
      "comments_count": 0,
      "user": {
        "username": "jsavigny",
        "id": 1,
        "karma": 4
      },
      "tags": [
        {
          "name": "Video",
          "description": "Video"
        }
      ]
    },

  ]
  "message": "Trending Topics"
}
```


This endpoint retrieves all topics, sticky and non sticky alike, sorted by trending or recency.

### HTTP Request

`GET http://api.local.host:5000/komunitas/v1/topics `

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
`tag` | 'Semua' | The tag to filter the topics.
`filter` | - | If filter = recent,then the response will return topics sorted by recency (recent topics), else sorted by trending (trending topics)
`page` | - | Pagination, each page will return 10 topics

## Get a Specific Topic

> Sample Request

```ruby
GET komunitas/v1/topics/1
Host: api.local.host:5000
```

```shell
curl "http://api.local.host:5000/komunitas/v1/topics/1"
```

> Sample Response

```json
{
  "status": "OK",
  "topic": {
    "id": 1,
    "short_id": "ez0iyc",
    "title": "Now I am become death",
    "description": "The destroyer of THE WORLD",
    "markeddown_description": "<p>The destroyer of THE WORLD</p>\n",
    "created_at": "2016-06-15T19:35:14.000+07:00",
    "updated_at": "2016-06-15T19:35:14.000+07:00",
    "upvotes": 2,
    "downvotes": 0,
    "comments_count": 0,
    "user": {
      "username": "jsavigny",
      "id": 1,
      "karma": 4
    },
    "tags": [
      {
        "name": "Video",
        "description": "Video"
      }
    ]
  },
  "comments": [
    {
      "id": 17,
      "short_id": "jdzxuy",
      "comment": "ea",
      "markeddown_comment": "<p>ea</p>\n",
      "created_at": "2016-06-17T10:56:35.000+07:00",
      "updated_at": "2016-06-17T10:56:35.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "user": {
        "username": "juliosavigny",
        "id": 2
      }
    }
  ],
  "message": "Topic details"
}
```

This endpoint retrieves a specific detailed topic, with its comments (if exist).


### HTTP Request

`GET http://api.local.host:5000/komunitas/v1/topics/:id`

### URL Parameters

Parameter | Description
--------- | -----------
`:id` | The ID of the topic to retrieve

## Create a topic

> Sample Request

```ruby
POST komunitas/v1/topics
Host: api.local.host:5000
Authorization: Basic user_id:api_token
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
curl -X POST "api.local.host:5000/komunitas/v1/topics"
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

`POST http://api.local.host:5000/komunitas/v1/topics/`

### URL Parameters

Parameter |        |Description
--------- | -------- |-----------
`title` | required |Title of the topic
`tags_a` | required |Tags of the topic
`description` | required | Body/description of the topic

## Upvote a topic

> Sample Request

```ruby
POST komunitas/v1/topics/1/upvotes
Host: apikomunitas.local.host:5000
Authorization: Basic user_id:api_token
```

```shell
curl -X POST "api.local.host:5000/komunitas/v1/topics/1/upvotes"
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

`POST http://api.local.host:5000/komunitas/v1/topics/:id/upvotes`

### URL Parameters

Parameter |        |Description
--------- | -------- |-----------
`:id` | required |id of the topic

## Downvote a topic

> Sample Request

```ruby
POST komunitas/v1/topics/1/downvotes
Host: api.local.host:5000:5000
Authorization: Basic user_id:api_token
```

```json
{
  "reason":"O"
}
```

```shell
curl -X POST "api.local.host:5000/komunitas/v1/topics/1/downvotes"
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

`POST http://api.local.host:5000/komunitas/v1/topics/:id/downvotes`

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
POST komunitas/v1/topics/1/unvotes
Host: api.local.host:5000
Authorization: Basic user_id:api_token
```

```shell
curl -X POST "api.local.host:5000/komunitas/v1/topics/1/unvotes"
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

`POST http://api.local.host:5000/komunitas/v1/topics/:id/unvotes`

### URL Parameters

Parameter |        |Description
--------- | -------- |-----------
`:id` | required |id of the topic
