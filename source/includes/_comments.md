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
      "id": 239,
      "comment": "Combo BREAKERRRRR",
      "markeddown_comment": "<p>Combo BREAKERRRRR</p>\n",
      "created_at": "2016-07-26T09:33:00.000+07:00",
      "updated_at": "2016-07-26T09:33:00.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": 1,
      "is_gone": false,
      "is_editable": true,
      "is_deletable": true,
      "is_undeletable": true,
      "user": {
        "username": "rahmanadianto",
        "id": 3,
        "karma": 19,
        "avatar": "http://www.local.host:5000/images/default_avatar/small/default.jpg"
      },
      "topic": {
        "title": "Hey Jude!",
        "id": 92
      }
    },
    {
      "id": 238,
      "comment": "Then you can start, to make it better..",
      "markeddown_comment": "<p>Then you can start, to make it better..</p>\n",
      "created_at": "2016-07-26T09:32:54.000+07:00",
      "updated_at": "2016-07-26T09:32:54.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": 1,
      "is_gone": false,
      "is_editable": true,
      "is_deletable": true,
      "is_undeletable": true,
      "user": {
        "username": "rahmanadianto",
        "id": 3,
        "karma": 19,
        "avatar": "http://www.local.host:5000/images/default_avatar/small/default.jpg"
      },
      "topic": {
        "title": "Hey Jude!",
        "id": 92
      }
    },
    {
      "id": 237,
      "comment": "Remember, to let her into your heart.",
      "markeddown_comment": "<p>Remember, to let her into your heart.</p>\n",
      "created_at": "2016-07-26T09:32:36.000+07:00",
      "updated_at": "2016-07-26T09:32:36.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": 1,
      "is_gone": false,
      "is_editable": true,
      "is_deletable": true,
      "is_undeletable": true,
      "user": {
        "username": "rahmanadianto",
        "id": 3,
        "karma": 19,
        "avatar": "http://www.local.host:5000/images/default_avatar/small/default.jpg"
      },
      "topic": {
        "title": "Hey Jude!",
        "id": 92
      }
    },
    {
      "id": 236,
      "comment": "And make it better..",
      "markeddown_comment": "<p>And make it better..</p>\n",
      "created_at": "2016-07-26T09:31:59.000+07:00",
      "updated_at": "2016-07-26T09:31:59.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": 1,
      "is_gone": false,
      "is_editable": true,
      "is_deletable": true,
      "is_undeletable": true,
      "user": {
        "username": "rahmanadianto",
        "id": 3,
        "karma": 19,
        "avatar": "http://www.local.host:5000/images/default_avatar/small/default.jpg"
      },
      "topic": {
        "title": "Hey Jude!",
        "id": 92
      }
    },
    {
      "id": 235,
      "comment": "Take a sad song..",
      "markeddown_comment": "<p>Take a sad song..</p>\n",
      "created_at": "2016-07-26T09:31:51.000+07:00",
      "updated_at": "2016-07-26T09:31:51.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": 1,
      "is_gone": false,
      "is_editable": true,
      "is_deletable": true,
      "is_undeletable": true,
      "user": {
        "username": "rahmanadianto",
        "id": 3,
        "karma": 19,
        "avatar": "http://www.local.host:5000/images/default_avatar/small/default.jpg"
      },
      "topic": {
        "title": "Hey Jude!",
        "id": 92
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
GET komunitas/comments/235
Host: api.local.host:5000
```

```shell
curl "http://api.local.host:5000/komunitas/comments/235"
```

> Sample Response

```json
{
  "status": "OK",
  "comment": {
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
    },
    "topic": {
      "title": "Hey Jude!",
      "id": 92
    }
  },
  "child_comments": [
    {
      "id": 236,
      "comment": "And make it better..",
      "markeddown_comment": "<p>And make it better..</p>\n",
      "upvotes": 1,
      "downvotes": 0,
      "vote": 1,
      "created_at": "2016-07-26T09:31:59.000+07:00",
      "updated_at": "2016-07-26T09:31:59.000+07:00",
      "parent_comment_id": 235,
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
    },
    {
      "id": 237,
      "comment": "Remember, to let her into your heart.",
      "markeddown_comment": "<p>Remember, to let her into your heart.</p>\n",
      "upvotes": 1,
      "downvotes": 0,
      "vote": 1,
      "created_at": "2016-07-26T09:32:36.000+07:00",
      "updated_at": "2016-07-26T09:32:36.000+07:00",
      "parent_comment_id": 236,
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
    },
    {
      "id": 238,
      "comment": "Then you can start, to make it better..",
      "markeddown_comment": "<p>Then you can start, to make it better..</p>\n",
      "upvotes": 1,
      "downvotes": 0,
      "vote": 1,
      "created_at": "2016-07-26T09:32:54.000+07:00",
      "updated_at": "2016-07-26T09:32:54.000+07:00",
      "parent_comment_id": 237,
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
    },
    {
      "id": 239,
      "comment": "Comment removed by author",
      "markeddown_comment": "Comment removed by author",
      "upvotes": null,
      "downvotes": null,
      "vote": null,
      "created_at": "2016-07-26T09:33:00.000+07:00",
      "updated_at": "2016-07-26T09:33:00.000+07:00",
      "parent_comment_id": 238,
      "is_editable": true,
      "is_deletable": true,
      "is_undeletable": true,
      "is_gone": true,
      "user": {
        "username": "rahmanadianto",
        "id": 3,
        "karma": 19,
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
  "message": "Not Found"
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

## Edit a comment

> Sample Request

```ruby
PATCH komunitas/comment/19
Host: api.local.host:5000
Authorization: Basic user_id:api_token
Content-Type Application/JSON
```

```json
{
    "comment":"Edited"
}
```

```shell
curl -X POST "api.local.host:5000/komunitas/comments/19"
        -d  '{
                "comment":"Edited"
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
  "message": "Comment Edited"
}
```

> Authentication Error response

```json
{
  "status": "ERROR",
  "message": "Anda harus login untuk mengakses halaman ini"
}
```

> Not Found Error Response

```json
{
  "status": "ERROR",
  "message": "Not Found"
}
```

> Not Permitted Error

```json
{
  "status": "ERROR",
  "message": "Not Permitted"
}
```

This endpoint is used to edit a comment.
A comment can be edited by the author of the comment if the comment is still recent, or by moderators and administrators.
<aside class="notice"> Requires Authentication </aside>


### HTTP Request

`PATCH http://api.local.host:5000/komunitas/comments/:id`

### URL Parameters

Parameter |        |Description
--------- | ------------ |-----------
`comment` | required |The comment
`:id` | required | id of the comment

## Delete a comment

> Sample Request

```ruby
DELETE komunitas/comments/1
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
```
> Success Response

```json
{
  "status": "OK",
  "message": "Comment Deleted"
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

This endpoint is used to delete a comment.
A comment can be deleted by the author of the comment, or by moderators and administrators.

<aside class="notice"> Requires Authentication </aside>


### HTTP Request

`DELETE http://api.local.host:5000/komunitas/comments/:id`

### URL Parameters

Parameter |        |Description
--------- | -------- |-----------
`:id` | required |id of the topic
`moderation_reason` |  | reason for deletion

## Undelete a topic

> Sample Request

```ruby
POST komunitas/comments/1/restoration
Host: api.local.host:5000
Authorization: Basic user_id:api_token
```

```shell
curl -X POST "api.local.host:5000/komunitas/comments/1/restoration"
      -u "1:RnLxZ69SP0tOmJoulmG7"
```
> Success Response

```json
{
  "status": "OK",
  "message": "Comment Undeleted"
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

This endpoint is used to undelete a comment.
A comment can be undeleted if the comment is gone (deleted) by the author of the comment, or by moderators/admins.
<aside class="notice"> Requires Authentication </aside>


### HTTP Request

`POST http://api.local.host:5000/komunitas/comments/:id/restoration`

### URL Parameters

Parameter |        |Description
--------- | -------- |-----------
`:id` | required |id of the topic

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
