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
          "tag": "Video",
          "description": "Video"
        }
      ]
    },
    {
      "id": 4,
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
          "tag": "Video",
          "description": "Video"
        }
      ]
    }
  ],
  "sticky_topics": [   
    {
      "id": 3,
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
          "tag": "Video",
          "description": "Video"
        }
      ]
    },

  ],
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
    "title": "Yea",
    "description": "Instagram",
    "markeddown_description": "<p>Instagram</p>\n",
    "created_at": "2016-06-23T09:51:37.000+07:00",
    "updated_at": "2016-06-23T09:51:37.000+07:00",
    "upvotes": 1,
    "downvotes": 0,
    "comments_count": 2,
    "user": {
      "username": "jsavigny",
      "id": 1,
      "karma": 0
    },
    "tags": [
      {
        "tag": "Komputer",
        "description": "Magic Box"
      },
      {
        "name": "Kamera",
        "description": "Double tap to love"
      }
    ]
  },
  "comments": [
    {
      "id": 2,
      "comment": "Jelek sekarang logonya",
      "markeddown_comment": "<p>Jelek sekarang logonya</p>\n",
      "created_at": "2016-06-23T09:51:45.000+07:00",
      "updated_at": "2016-06-23T09:51:45.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "parent_comment_id": null,
      "user": {
        "username": "jsavigny",
        "id": 1,
        "karma": 0
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

`POST http://api.local.host:5000/komunitas/v1/topics/`

### URL Parameters

Parameter |        |Description
--------- | -------- |-----------
`title` | required |Title of the topic
`tags_a` | required |Tags of the topic
`description` | required | Body/description of the topic

## Preview a topic

> Sample Request

```ruby
POST komunitas/v1/topics/preview
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
Host: api.local.host:5000
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
Host: api.local.host:5000
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