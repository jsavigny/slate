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
      "id": 17,
      "comment": "ea",
      "markeddown_comment": "<p>ea</p>\n",
      "short_id": "jdzxuy",
      "created_at": "2016-06-17T10:56:35.000+07:00",
      "updated_at": "2016-06-17T10:56:35.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "parent_comment_id": null,
      "user": {
        "username": "juliosavigny",
        "id": 2,
        "karma": -1
      },
      "topic": {
        "title": "Now I am become death",
        "id": 1
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

## Create a comment

> Sample Request

```ruby
POST /v1/comments
Host: apikomunitas.local.host:5000
Authorization: Basic user_id:api_token
```

```json
{
    "comment":"What?",
    "story_id":1
}
```

```shell
curl -X POST "apikomunitas.local.host:5000/v1/topics"
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
curl -X POST "apikomunitas.local.host:5000/v1/topics"
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
  "comment": {
    "id": null,
    "story_id": null,
    "parent_comment_id": null
  },
  "message": "Story Not Found"
}
```
> Invalid Parent Comment Error response

```json
{
  "status": "ERROR",
  "comment": {
    "id": null,
    "story_id": null,
    "parent_comment_id": null
  },
  "message": "Invalid Parent Comment"
}
```
> Recently commented here Error response

```json
{
  "status": "ERROR",
  "comment": {
    "id": null,
    "story_id": null,
    "parent_comment_id": null
  },
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

`POST http://apikomunitas.local.host:5000/v1/comments/`

### URL Parameters

Parameter |        |Description
--------- | ------------ |-----------
`comment` | required |The comment
`story_id` | required | id of the story that you're commenting
`parent_comment_id` | not required | id of the comment that you're replying to
