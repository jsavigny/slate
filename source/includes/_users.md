# Users

## Get Specific User Profile

> Sample Request

```ruby
GET komunitas/users/1
Host: api.local.host:5000
```

```shell
curl "http://api.local.host:5000/komunitas/tags"
```

> Sample Response


```json
{
  "status": "OK",
  "user": {
    "id": 2,
    "username": "juliosavigny",
    "avatar": "http://www.local.host:5000/system4/avatars/1/small/250px-Stannis_sigil_coat.png",
    "name": "Julio Savigny",
    "karma": 2,
    "topics_count": 4,
    "comments_count": 12,
    "is_banned": false,
    "is_admin": false,
    "is_moderator": false,
    "is_active": true,
    "created_at": "2016-06-23T14:26:19.000+07:00",
    "description": null
  },
  "message": "User Profile"
}
```

> Not Found Response

```json
{
  "status": "ERROR",
  "message": "Not Found"
}
```


This endpoint retrieves user profile.

### HTTP Request

`GET http://api.local.host/komunitas/users `

## Get All Topics posted by a User

> Sample Request

```ruby
GET komunitas/users/1/topics?&page=1
Host: api.local.host:5000
```

```shell
curl "http://api.local.host:5000/komunitas/users/1/topics?&page=1"
```


> Sample Response

```json
{
  "status": "OK",
  "topics": [
    {
      "id": 9,
      "title": "Topik 1",
      "created_at": "2016-06-29T10:53:10.000+07:00",
      "updated_at": "2016-06-30T10:12:43.000+07:00",
      "upvotes": 2,
      "downvotes": 0,
      "vote": 1,
      "comments_count": 2,
      "is_sticky": false,
      "user": {
        "username": "jsavigny",
        "id": 1,
        "karma": 2
      },
      "tags": [
        {
          "tag": "Video",
          "description": "Bukan XXX"
        }
      ]
    },
    {
      "id": 10,
      "title": "Topik 2",
      "created_at": "2016-06-29T10:53:42.000+07:00",
      "updated_at": "2016-06-29T10:55:41.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": 1,
      "comments_count": 4,
      "is_sticky": false,
      "user": {
        "username": "jsavigny",
        "id": 1,
        "karma": 2
      },
      "tags": [
        {
          "tag": "Pengumuman",
          "description": "Hello, World!"
        }
      ]
    },
    {
      "id": 12,
      "title": "Topik 4",
      "created_at": "2016-06-29T10:54:44.000+07:00",
      "updated_at": "2016-06-29T10:54:44.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": 1,
      "comments_count": 1,
      "is_sticky": false,
      "user": {
        "username": "jsavigny",
        "id": 1,
        "karma": 2
      },
      "tags": [
        {
          "tag": "Kamera",
          "description": "Double tap to love"
        }
      ]
    },
    {
      "id": 13,
      "title": "Topik 5",
      "created_at": "2016-06-29T10:55:01.000+07:00",
      "updated_at": "2016-06-29T10:55:01.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": 1,
      "comments_count": 2,
      "is_sticky": false,
      "user": {
        "username": "jsavigny",
        "id": 1,
        "karma": 2
      },
      "tags": [
        {
          "tag": "Komputer",
          "description": "Magic Box"
        }
      ]
    },
    {
      "id": 14,
      "title": "Topik 6",
      "created_at": "2016-06-30T10:11:26.000+07:00",
      "updated_at": "2016-06-30T10:11:26.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": 1,
      "comments_count": 0,
      "is_sticky": false,
      "user": {
        "username": "jsavigny",
        "id": 1,
        "karma": 2
      },
      "tags": [
        {
          "tag": "Sepeda",
          "description": "I want to ride my bicycle~"
        }
      ]
    },
    {
      "id": 15,
      "title": "Topik 7",
      "created_at": "2016-06-30T10:11:41.000+07:00",
      "updated_at": "2016-06-30T10:11:41.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": 1,
      "comments_count": 1,
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
      "id": 16,
      "title": "Topik 8",
      "created_at": "2016-06-30T10:12:06.000+07:00",
      "updated_at": "2016-06-30T10:12:06.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": 1,
      "comments_count": 0,
      "is_sticky": false,
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
    },
    {
      "id": 17,
      "title": "Topik Test",
      "created_at": "2016-06-30T11:35:31.000+07:00",
      "updated_at": "2016-06-30T11:35:31.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": 1,
      "comments_count": 0,
      "is_sticky": false,
      "user": {
        "username": "jsavigny",
        "id": 1,
        "karma": 2
      },
      "tags": [
        {
          "tag": "Pengumuman",
          "description": "Hello, World!"
        }
      ]
    }
  ],
  "message": "User Topics"
}
```


This endpoint retrieves all topics posted by specific user.

### HTTP Request

`GET http://api.local.host:5000/komunitas/users/:id/topics `

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
`id` | - | id of the user
`page` | - | Pagination, each page will return 8 topics

## Get All Comments posted by a User

> Sample Request

```ruby
GET komunitas/users/1/comments?page=1
Host: api.local.host:5000
```

```shell
curl "http://api.local.host:5000/komunitas/users/1/comments?page=1"
```

> Sample Response


```json

{
  "status": "OK",
  "comments": [
    {
      "id": 4,
      "comment": "Apa isi nya? masa kosong? Bego nih",
      "markeddown_comment": "<p>Apa isi nya? masa kosong? Bego nih</p>\n",
      "created_at": "2016-06-29T10:55:18.000+07:00",
      "updated_at": "2016-06-29T10:55:18.000+07:00",
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
        "title": "Topik 2",
        "id": 10
      }
    },
    {
      "id": 5,
      "comment": "Iya nih, bego",
      "markeddown_comment": "<p>Iya nih, bego</p>\n",
      "created_at": "2016-06-29T10:56:01.000+07:00",
      "updated_at": "2016-06-29T10:56:01.000+07:00",
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
        "title": "Topik 2",
        "id": 10
      }
    },
    {
      "id": 15,
      "comment": "hmmmmm",
      "markeddown_comment": "<p>hmmmmm</p>\n",
      "created_at": "2016-07-01T07:21:04.000+07:00",
      "updated_at": "2016-07-01T07:21:04.000+07:00",
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
        "title": "Topik 2",
        "id": 10
      }
    },
    {
      "id": 19,
      "comment": "apa hm hm",
      "markeddown_comment": "<p>apa hm hm</p>\n",
      "created_at": "2016-07-11T10:12:08.000+07:00",
      "updated_at": "2016-07-11T10:12:08.000+07:00",
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
        "title": "Topik 2",
        "id": 10
      }
    },
    {
      "id": 6,
      "comment": "Tes",
      "markeddown_comment": "<p>Tes</p>\n",
      "created_at": "2016-06-30T11:04:12.000+07:00",
      "updated_at": "2016-06-30T11:04:12.000+07:00",
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
        "title": "Topik 1",
        "id": 9
      }
    },
    {
      "id": 7,
      "comment": "Console peasant!",
      "markeddown_comment": "<p>Console peasant!</p>\n",
      "created_at": "2016-06-30T11:04:23.000+07:00",
      "updated_at": "2016-06-30T11:04:23.000+07:00",
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
        "title": "Topik 5",
        "id": 13
      }
    },
    {
      "id": 10,
      "comment": "All hail Gaben!",
      "markeddown_comment": "<p>All hail Gaben!</p>\n",
      "created_at": "2016-06-30T11:05:16.000+07:00",
      "updated_at": "2016-06-30T11:05:16.000+07:00",
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
        "title": "Topik 5",
        "id": 13
      }
    },
    {
      "id": 8,
      "comment": "Yoi",
      "markeddown_comment": "<p>Yoi</p>\n",
      "created_at": "2016-06-30T11:04:38.000+07:00",
      "updated_at": "2016-06-30T11:04:38.000+07:00",
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
        "title": "Topik 7",
        "id": 15
      }
    }
  ],
  "message": "User Profile"
}
```


This endpoint retrieves all comments posted by a specific user.

### HTTP Request

`GET http://api.local.host/komunitas/users/:id/comments `

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
`id` | - | id of the user
`page` | - | Pagination, each page will return 8 comments.

## Freeze/Unfreeze User forum activity

> Sample Request

```ruby
PATCH komunitas/user/3
Host: api.local.host:5000
Authorization: Basic user_id:api_token
```

```shell
curl -X POST "api.local.host:5000/komunitas/user/3"
      -u "1:RnLxZ69SP0tOmJoulmG7"
```

> Freeze Success Response

```json
{
  "status": "OK",
  "message": "User telah di-freeze"
}
```

> Unfreeze Success Response

```json
{
  "status": "OK",
  "message": "User telah di-unfreeze"
}
```

> Not Found Error

```json
{
  "status": "ERROR",
  "message": "Not Found"
}
```

> Authentication Error

```json
{
  "status": "ERROR",
  "message": "Anda harus login untuk mengakses halaman ini"
}
```

This endpoint is used to freeze or unfreeze a user forum activity.
Only moderators and admins can do this actions.
<aside class="notice"> Requires Authentication </aside>


### HTTP Request

`POST http://api.local.host:5000/komunitas/topics/:id/unvotes`

### URL Parameters

Parameter |        |Description
--------- | -------- |-----------
`:id` | required |id of the topic
