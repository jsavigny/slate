# Comments

## Get All Comments

> Sample Request

```ruby
GET komunitas/comments
Host: api.bukalapak.com
```

```shell
curl "http://api.bukalapak.com/komunitas/comments"
```

> Sample Response


```json
{
  "status": "OK",
  "comments": [
    {
      "id": 138,
      "comment": "YAA @jsavigny",
      "markeddown_comment": "<p>YAA <a href=\"/u/jsavigny\">@jsavigny</a></p>\n",
      "created_at": "2016-08-12T15:26:15.000+07:00",
      "updated_at": "2016-08-12T15:26:15.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "can_downvote": true,
      "vote": null,
      "is_gone": false,
      "is_editable": true,
      "is_deletable": true,
      "is_undeletable": true,
      "user": {
        "username": "juliosavigny",
        "id": 517,
        "karma": 1,
        "avatar": "http://www.staging.vm:5000/images/default_avatar/small/default.jpg"
      },
      "topic": {
        "title": "Topik Mention FCM",
        "id": 43
      }
    },
    {
      "id": 137,
      "comment": "@jsavigny",
      "markeddown_comment": "<p><a href=\"/u/jsavigny\">@jsavigny</a></p>\n",
      "created_at": "2016-08-12T15:25:20.000+07:00",
      "updated_at": "2016-08-12T15:25:20.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "can_downvote": true,
      "vote": null,
      "is_gone": false,
      "is_editable": true,
      "is_deletable": true,
      "is_undeletable": true,
      "user": {
        "username": "juliosavigny",
        "id": 517,
        "karma": 1,
        "avatar": "http://www.staging.vm:5000/images/default_avatar/small/default.jpg"
      },
      "topic": {
        "title": "Topik Mention FCM",
        "id": 43
      }
    },
    {
      "id": 136,
      "comment": "mantap",
      "markeddown_comment": "<p>mantap</p>\n",
      "created_at": "2016-08-12T13:17:00.000+07:00",
      "updated_at": "2016-08-12T13:17:00.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "can_downvote": true,
      "vote": null,
      "is_gone": false,
      "is_editable": true,
      "is_deletable": true,
      "is_undeletable": true,
      "user": {
        "username": "jsavigny",
        "id": 514,
        "karma": 2,
        "avatar": "http://www.staging.vm:5000/images/default_avatar/small/default.jpg"
      },
      "topic": {
        "title": "Riwayat Pemotongan Budget Promoted Push Tidak Informatif?",
        "id": 14
      }
    },
    {
      "id": 135,
      "comment": "sans",
      "markeddown_comment": "<p>sans</p>\n",
      "created_at": "2016-08-12T13:16:32.000+07:00",
      "updated_at": "2016-08-12T13:16:32.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "can_downvote": true,
      "vote": null,
      "is_gone": false,
      "is_editable": true,
      "is_deletable": true,
      "is_undeletable": true,
      "user": {
        "username": "jsavigny",
        "id": 514,
        "karma": 2,
        "avatar": "http://www.staging.vm:5000/images/default_avatar/small/default.jpg"
      },
      "topic": {
        "title": "Riwayat Pemotongan Budget Promoted Push Tidak Informatif?",
        "id": 14
      }
    },
    {
      "id": 134,
      "comment": "@jsavigny",
      "markeddown_comment": "<p><a href=\"/u/jsavigny\">@jsavigny</a></p>\n",
      "created_at": "2016-08-12T11:25:50.000+07:00",
      "updated_at": "2016-08-12T11:25:50.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "can_downvote": true,
      "vote": null,
      "is_gone": false,
      "is_editable": true,
      "is_deletable": true,
      "is_undeletable": true,
      "user": {
        "username": "quinsythecat",
        "id": 519,
        "karma": 0,
        "avatar": "http://www.staging.vm:5000/images/default_avatar/small/default.jpg"
      },
      "topic": {
        "title": "Riwayat Pemotongan Budget Promoted Push Tidak Informatif?",
        "id": 14
      }
    },
    {
      "id": 133,
      "comment": "kucing @jsavigny",
      "markeddown_comment": "<p>kucing <a href=\"/u/jsavigny\">@jsavigny</a></p>\n",
      "created_at": "2016-08-12T11:24:43.000+07:00",
      "updated_at": "2016-08-12T11:24:43.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "can_downvote": true,
      "vote": null,
      "is_gone": false,
      "is_editable": true,
      "is_deletable": true,
      "is_undeletable": true,
      "user": {
        "username": "quinsythecat",
        "id": 519,
        "karma": 0,
        "avatar": "http://www.staging.vm:5000/images/default_avatar/small/default.jpg"
      },
      "topic": {
        "title": "Riwayat Pemotongan Budget Promoted Push Tidak Informatif?",
        "id": 14
      }
    },
    {
      "id": 132,
      "comment": "https://komunitas.bukalapak.com/s/q2sran/ini_dia_pemenang_kontes_menulis_serunya_kopdar_bareng_komunitas_bukalapak_periode_juli",
      "markeddown_comment": "<p><a href=\"https://komunitas.bukalapak.com/s/q2sran/ini_dia_pemenang_kontes_menulis_serunya_kopdar_bareng_komunitas_bukalapak_periode_juli\" target=\"_blank\" rel=\"nofollow\">https://komunitas.bukalapak.com/s/q2sran/ini_dia_pemenang_kontes_menulis_serunya_kopdar_bareng_komunitas_bukalapak_periode_juli</a></p>\n",
      "created_at": "2016-08-12T11:14:01.000+07:00",
      "updated_at": "2016-08-12T11:14:01.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "can_downvote": true,
      "vote": null,
      "is_gone": false,
      "is_editable": true,
      "is_deletable": true,
      "is_undeletable": true,
      "user": {
        "username": "juliosavigny",
        "id": 517,
        "karma": 1,
        "avatar": "http://www.staging.vm:5000/images/default_avatar/small/default.jpg"
      },
      "topic": {
        "title": "Deeplink test",
        "id": 50
      }
    },
    {
      "id": 131,
      "comment": "josgandos!",
      "markeddown_comment": "<p>josgandos!</p>\n",
      "created_at": "2016-08-12T11:07:02.000+07:00",
      "updated_at": "2016-08-12T11:07:02.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "can_downvote": true,
      "vote": null,
      "is_gone": false,
      "is_editable": true,
      "is_deletable": true,
      "is_undeletable": true,
      "user": {
        "username": "jsavigny",
        "id": 514,
        "karma": 2,
        "avatar": "http://www.staging.vm:5000/images/default_avatar/small/default.jpg"
      },
      "topic": {
        "title": "Masih Ada Aja Pembeli Yang Marah-Marah di Forum Komunitas Gara-Gara Barang Belum Nyampai",
        "id": 19
      }
    }
  ],
  "message": "Comments"
}```


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
GET komunitas/comments/42
Host: api.bukalapak.com
```

```shell
curl "http://api.bukalapak.com/komunitas/comments/42"
```

> Sample Response

```json
{
  "status": "OK",
  "comment": {
    "id": 42,
    "comment": "Iya nih, mari jadi smart buyer!",
    "markeddown_comment": "<p>Iya nih, mari jadi smart buyer!</p>\n",
    "upvotes": 2,
    "downvotes": 0,
    "vote": null,
    "can_downvote": true,
    "created_at": "2016-08-11T10:13:37.000+07:00",
    "updated_at": "2016-08-11T10:13:37.000+07:00",
    "parent_comment_id": null,
    "is_editable": true,
    "is_deletable": true,
    "is_undeletable": true,
    "is_gone": false,
    "user": {
      "username": "juliosavigny",
      "id": 517,
      "karma": 1,
      "avatar": "http://www.staging.vm:5000/images/default_avatar/small/default.jpg"
    },
    "topic": {
      "title": "Masih Ada Aja Pembeli Yang Marah-Marah di Forum Komunitas Gara-Gara Barang Belum Nyampai",
      "id": 19
    }
  },
  "child_comments": [
    {
      "id": 131,
      "comment": "josgandos!",
      "markeddown_comment": "<p>josgandos!</p>\n",
      "upvotes": 1,
      "downvotes": 0,
      "vote": null,
      "can_downvote": true,
      "created_at": "2016-08-12T11:07:02.000+07:00",
      "updated_at": "2016-08-12T11:07:02.000+07:00",
      "parent_comment_id": 42,
      "is_editable": true,
      "is_deletable": true,
      "is_undeletable": true,
      "is_gone": false,
      "user": {
        "username": "jsavigny",
        "id": 514,
        "karma": 2,
        "avatar": "http://www.staging.vm:5000/images/default_avatar/small/default.jpg"
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

`GET http://api.bukalapak.com/komunitas/comments/:id`

### URL Parameters

Parameter | Description
--------- | -----------
`:id` | The ID of the comment to retrieve

## Create a comment

> Sample Request

```ruby
POST komunitas/comments
Host: api.bukalapak.com
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
curl -X POST "api.bukalapak.com/komunitas/topics"
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
curl -X POST "api.bukalapak.com/komunitas/topics"
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

`POST http://api.bukalapak.com/komunitas/comments/`

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
Host: api.bukalapak.com
Authorization: Basic user_id:api_token
Content-Type Application/JSON
```

```json
{
    "comment":"Edited"
}
```

```shell
curl -X PATCH "api.bukalapak.com/komunitas/comments/19"
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

`PATCH http://api.bukalapak.com/komunitas/comments/:id`

### URL Parameters

Parameter |        |Description
--------- | ------------ |-----------
`comment` | required |The comment
`:id` | required | id of the comment

## Delete a comment

> Sample Request

```ruby
PATCH komunitas/comments/1/deletion
Host: api.bukalapak.com
Authorization: Basic user_id:api_token
```

```json
{
    "moderation_reason": "reason"
}
```

```shell
curl -X POST "api.bukalapak.com/komunitas/comments/1/deletion"
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

`PATCH http://api.bukalapak.com/komunitas/comments/:id/deletion`

### URL Parameters

Parameter |        |Description
--------- | -------- |-----------
`:id` | required |id of the topic
`moderation_reason` |  | reason for deletion

## Undelete a topic

> Sample Request

```ruby
POST komunitas/comments/1/restoration
Host: api.bukalapak.com
Authorization: Basic user_id:api_token
```

```shell
curl -X POST "api.bukalapak.com/komunitas/comments/1/restoration"
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

`POST http://api.bukalapak.com/komunitas/comments/:id/restoration`

### URL Parameters

Parameter |        |Description
--------- | -------- |-----------
`:id` | required |id of the topic

## Upvote a comment

> Sample Request

```ruby
POST komunitas/comments/1/upvotes
Host: api.bukalapak.com
Authorization: Basic user_id:api_token
```

```shell
curl -X POST "api.bukalapak.com/komunitas/comments/1/upvotes"
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

`POST http://api.bukalapak.com/komunitas/comments/:id/upvotes`

### URL Parameters

Parameter |        |Description
--------- | -------- |-----------
`:id` | required |id of the comment

## Downvote a comment

> Sample Request

```ruby
POST komunitas/comments/1/downvotes
Host: api.bukalapak.com
Authorization: Basic user_id:api_token
```

```json
{
  "reason":"O"
}
```

```shell
curl -X POST "api.bukalapak.com/komunitas/comments/1/downvotes"
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

`POST http://api.bukalapak.com/komunitas/comments/:id/downvotes`

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
Host: api.bukalapak.com
Authorization: Basic user_id:api_token
```

```shell
curl -X POST "api.bukalapak.com/komunitas/comments/1/unvotes"
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

`POST http://api.bukalapak.com/komunitas/comments/:id/unvotes`

### URL Parameters

Parameter |        |Description
--------- | -------- |-----------
`:id` | required |id of the comment
