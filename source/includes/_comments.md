# Comments

## Get All Comments

> Sample Request

```ruby
GET komunitas/v1/comments
Host: api.local.host:5000
```

```shell
curl "http://api.local.host:5000/komunitas//comments"
```

> Sample Response


```json

{
  "status": "OK",
  "comments": [
    {
      "id": 3,
      "comment": "iya sekarang jelek :(",
      "markeddown_comment": "<p>iya sekarang jelek :(</p>\n",
      "created_at": "2016-06-23T10:22:48.000+07:00",
      "updated_at": "2016-06-23T10:22:48.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "user": {
        "username": "jsavigny",
        "id": 1,
        "karma": 0
      },
      "topic": {
        "title": "Yea",
        "id": 1
      }
    },
    {
      "id": 2,
      "comment": "Jelek sekarang logonya",
      "markeddown_comment": "<p>Jelek sekarang logonya</p>\n",
      "created_at": "2016-06-23T09:51:45.000+07:00",
      "updated_at": "2016-06-23T09:51:45.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "user": {
        "username": "jsavigny",
        "id": 1,
        "karma": 0
      },
      "topic": {
        "title": "Yea",
        "id": 1
      }
    }
  ],
  "message": "Comments"
}

```


This endpoint retrieves all comments.

### HTTP Request

`GET http://api.local.host/komunitas//comments `

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
`tag` | 'Semua' | The tag to filter the comments.
`page` | - | Pagination, each page will return 10 comments.

## Get a Specific Comment

> Sample Request

```ruby
GET komunitas/v1/comments/16
Host: api.local.host:5000
```

```shell
curl "http://api.local.host:5000/komunitas//comments/16"
```

> Sample Response

```json
{
  "status": "OK",
  "comment": {
    "id": 16,
    "comment": "Soon I awaked, and there I was, veritably myself again",
    "markeddown_comment": "<p>Soon I awaked, and there I was, veritably myself again</p>\n",
    "created_at": "2016-07-01T08:13:03.000+07:00",
    "updated_at": "2016-07-01T08:13:03.000+07:00",
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
  "child_comments": [
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

`GET http://api.local.host:5000/komunitas//comments/:id`

### URL Parameters

Parameter | Description
--------- | -----------
`:id` | The ID of the comment to retrieve

## Create a comment

> Sample Request

```ruby
POST komunitas/v1/comments
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
curl -X POST "api.local.host:5000/komunitas//topics"
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
curl -X POST "api.local.host:5000/komunitas//topics"
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

`POST http://api.local.host:5000/komunitas//comments/`

### URL Parameters

Parameter |        |Description
--------- | ------------ |-----------
`comment` | required |The comment
`story_id` | required | id of the story that you're commenting
`parent_comment_id` | not required | id of the comment that you're replying to


## Upvote a comment

> Sample Request

```ruby
POST komunitas/v1/comments/1/upvotes
Host: api.local.host:5000
Authorization: Basic user_id:api_token
```

```shell
curl -X POST "api.local.host:5000/komunitas//comments/1/upvotes"
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

`POST http://api.local.host:5000/komunitas//comments/:id/upvotes`

### URL Parameters

Parameter |        |Description
--------- | -------- |-----------
`:id` | required |id of the comment

## Downvote a comment

> Sample Request

```ruby
POST komunitas/v1/comments/1/downvotes
Host: api.local.host:5000
Authorization: Basic user_id:api_token
```

```json
{
  "reason":"O"
}
```

```shell
curl -X POST "api.local.host:5000/komunitas//comments/1/downvotes"
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

`POST http://api.local.host:5000/komunitas//comments/:id/downvotes`

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
POST komunitas/v1/comments/1/unvotes
Host: api.local.host:5000
Authorization: Basic user_id:api_token
```

```shell
curl -X POST "api.local.host:5000/komunitas//comments/1/unvotes"
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

`POST http://api.local.host:5000/komunitas//comments/:id/unvotes`

### URL Parameters

Parameter |        |Description
--------- | -------- |-----------
`:id` | required |id of the comment
