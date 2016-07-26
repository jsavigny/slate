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
      "id": 92,
      "title": "Hey Jude!",
      "created_at": "2016-07-26T09:27:27.000+07:00",
      "updated_at": "2016-07-26T09:27:27.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": 1,
      "comments_count": 0,
      "is_sticky": false,
      "is_editable": true,
      "is_undeletable": false,
      "user": {
        "username": "rahmanadianto",
        "id": 3,
        "karma": 19
      },
      "tags": [
        {
          "tag": "Kamera",
          "description": "Double tap to love"
        }
      ]
    },
    {
      "id": 87,
      "title": "Coba Updated",
      "created_at": "2016-07-25T12:48:58.000+07:00",
      "updated_at": "2016-07-25T12:49:08.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": 1,
      "comments_count": 0,
      "is_sticky": false,
      "is_editable": false,
      "is_undeletable": false,
      "user": {
        "username": "rahmanadianto",
        "id": 3,
        "karma": 19
      },
      "tags": [
        {
          "tag": "Video",
          "description": "Bukan XXX"
        }
      ]
    },
    {
      "id": 82,
      "title": "Rest Updated",
      "created_at": "2016-07-25T11:25:18.000+07:00",
      "updated_at": "2016-07-25T11:25:32.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": 1,
      "comments_count": 0,
      "is_sticky": false,
      "is_editable": false,
      "is_undeletable": false,
      "user": {
        "username": "rahmanadianto",
        "id": 3,
        "karma": 19
      },
      "tags": [
        {
          "tag": "Video",
          "description": "Bukan XXX"
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
    "description": "Don't make it bad.",
    "markeddown_description": "<p>Don&rsquo;t make it bad.</p>\n",
    "id": 92,
    "title": "Hey Jude!",
    "created_at": "2016-07-26T09:27:27.000+07:00",
    "updated_at": "2016-07-26T09:27:27.000+07:00",
    "upvotes": 1,
    "downvotes": 0,
    "vote": 1,
    "comments_count": 5,
    "is_editable": true,
    "is_gone": false,
    "is_undeletable": true,
    "user": {
      "username": "rahmanadianto",
      "id": 3,
      "karma": 19
    },
    "tags": [
      {
        "tag": "Kamera",
        "description": "Double tap to love"
      }
    ]
  },
  "comments": [
    {
      "id": 235,
      "comment": "Take a sad song..",
      "markeddown_comment": "<p>Take a sad song..</p>\n",
      "upvotes": 1,
      "downvotes": 0,
      "vote": 1,
      "created_at": "2016-07-26T09:31:51.000+07:00",
      "updated_at": "2016-07-26T09:31:51.000+07:00",
      "parent_comment_id": null,
      "is_editable": true,
      "is_deletable": true,
      "is_undeletable": true,
      "is_gone": false,
      "user": {
        "username": "rahmanadianto",
        "id": 3,
        "karma": 19,
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
    "title":"Now I am become death"
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

## Edit a topic

> Sample Request

```ruby
PATCH komunitas/topics/1
Host: api.local.host:5000
Authorization: Basic user_id:api_token
```

```json
{
  "topic":{
          "title":"Coba Updated",
          "description":"Updated Description",
          "moderation_reason": "Reason"
  }
}
```

```shell
curl -X PATCH "api.local.host:5000/komunitas/topics/1"
      -u "1:RnLxZ69SP0tOmJoulmG7"
      -d  '{
            "topic":{
                    "title":"Coba Updated",
                    "description":"Updated Description",
                    "moderation_reason": "Reason"
            }
          }'
```
> Success Response

```json
{
  "status": "OK",
  "topic_detail": {
    "id": 1,
    "title":"Now I am become death"
  },
  "message": "Topic Edited"
}
```

> Authentication Error

```json
{
  "status": "ERROR",
  "message": "Anda harus login untuk mengakses halaman ini"
}
```

> Not Found Error

```json
{
  "status": "ERROR",
  "message": "Not Found"
}
```

> Unauthorized Error

```json
{
  "status": "ERROR",
  "message": "Anda tidak dapat mengakses halaman tersebut"
}
```

> Not Permitted Error

```json
{
  "status": "ERROR",
  "message": "Not Permitted"
}
```

This endpoint is used to edit a topic.
A topic can be edited by the author of the topic if the topic is still recent, or by moderators and administrators.

<aside class="notice"> Requires Authentication </aside>


### HTTP Request

`PATCH http://api.local.host:5000/komunitas/topics/:id`

### URL Parameters

Parameter |        |Description
--------- | -------- |-----------
`title` |   |Title of the topic
`tags_a` |   |Tags of the topic
`description` |   | Body/description of the topic
`moderation_reason` | only for moderators/admins | The reason for changes

## Delete a topic

> Sample Request

```ruby
DELETE komunitas/topics/1
Host: api.local.host:5000
Authorization: Basic user_id:api_token
```

```json
{
    "moderation_reason": "reason"
}
```

```shell
curl -X DELETE "api.local.host:5000/komunitas/topics/1"
      -u "1:RnLxZ69SP0tOmJoulmG7"
      -d  '{
            "moderation_reason": "reason"
          }'
```
> Success Response

```json
{
  "status": "OK",
  "message": "Topic Deleted"
}
```

> Authentication Error

```json
{
  "status": "ERROR",
  "message": "Anda harus login untuk mengakses halaman ini"
}
```

> Not Found Error

```json
{
  "status": "ERROR",
  "message": "Not Found"
}
```

> Unauthorized Error

```json
{
  "status": "ERROR",
  "message": "Anda tidak dapat mengakses halaman tersebut"
}
```

This endpoint is used to delete a topic.
A topic can be deleted by moderators and administrators.

<aside class="notice"> Requires Authentication </aside>


### HTTP Request

`DELETE http://api.local.host:5000/komunitas/topics/:id`

### URL Parameters

Parameter |        |Description
--------- | -------- |-----------
`:id` | required |id of the topic
`moderation_reason` |  | reason for deletion

## Undelete a topic

> Sample Request

```ruby
POST komunitas/topics/1/restoration
Host: api.local.host:5000
Authorization: Basic user_id:api_token
```

```shell
curl -X POST "api.local.host:5000/komunitas/topics/1/restoration"
      -u "1:RnLxZ69SP0tOmJoulmG7"
```
> Success Response

```json
{
  "status": "OK",
  "message": "Topic Undeleted"
}
```

> Authentication Error

```json
{
  "status": "ERROR",
  "message": "Anda harus login untuk mengakses halaman ini"
}
```

> Not Found Error

```json
{
  "status": "ERROR",
  "message": "Not Found"
}
```

> Unauthorized Error

```json
{
  "status": "ERROR",
  "message": "Anda tidak dapat mengakses halaman tersebut"
}
```

> Not Permitted Error

```json
{
  "status": "ERROR",
  "message": "Not Permitted"
}
```

This endpoint is used to undelete a topic.
A topic can be undeleted by moderators/admins if the topic is gone (deleted)
<aside class="notice"> Requires Authentication </aside>


### HTTP Request

`POST http://api.local.host:5000/komunitas/topics/:id/restoration`

### URL Parameters

Parameter |        |Description
--------- | -------- |-----------
`:id` | required |id of the topic


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
