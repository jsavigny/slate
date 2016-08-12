# Topics

## Get All Topics

> Sample Request

```ruby
GET komunitas/topics?filter=recent&page=1&tag=Semua
Host: api.bukalapak.com
```

```shell
curl "http://api.bukalapak.com/komunitas/topics?filter=recent&page=1&tag=Semua"
```


> Sample Response

```json
{
  "status": "OK",
  "topics": [
    {
      "id": 50,
      "title": "Deeplink test",
      "url": "http://komunitas.staging.vm:5000/s/juiegl/deeplink_test",
      "created_at": "2016-08-12T11:13:28.000+07:00",
      "updated_at": "2016-08-12T11:13:28.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": null,
      "comments_count": 1,
      "is_sticky": false,
      "is_editable": false,
      "is_gone": false,
      "is_undeletable": false,
      "user": {
        "username": "juliosavigny",
        "id": 517,
        "karma": 1
      },
      "tags": [
        {
          "tag": "Berita",
          "description": "Berbagi informasi terbaru yang sedang hangat-hangatnya"
        }
      ]
    },
    {
      "id": 49,
      "title": "Markeddown",
      "url": "http://komunitas.staging.vm:5000/s/xlooz5/markeddown",
      "created_at": "2016-08-12T11:05:01.000+07:00",
      "updated_at": "2016-08-12T11:05:01.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": null,
      "comments_count": 0,
      "is_sticky": false,
      "is_editable": false,
      "is_gone": false,
      "is_undeletable": false,
      "user": {
        "username": "ragapinilih",
        "id": 1,
        "karma": 2
      },
      "tags": [
        {
          "tag": "Pengumuman",
          "description": "Pengumuman dan pemberitahuan resmi dari tim Bukalapak"
        }
      ]
    },
    {
      "id": 48,
      "title": "Test to device",
      "url": "http://komunitas.staging.vm:5000/s/nkoq5t/test_to_device",
      "created_at": "2016-08-12T11:00:39.000+07:00",
      "updated_at": "2016-08-12T11:00:39.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": null,
      "comments_count": 0,
      "is_sticky": false,
      "is_editable": false,
      "is_gone": false,
      "is_undeletable": false,
      "user": {
        "username": "juliosavigny",
        "id": 517,
        "karma": 1
      },
      "tags": [
        {
          "tag": "Ide & Masalah Fitur",
          "description": "Sampaikan bug/error"
        }
      ]
    },
    {
      "id": 47,
      "title": "Test from device",
      "url": "http://komunitas.staging.vm:5000/s/ldrwuo/test_from_device",
      "created_at": "2016-08-12T10:59:47.000+07:00",
      "updated_at": "2016-08-12T10:59:47.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": null,
      "comments_count": 0,
      "is_sticky": false,
      "is_editable": false,
      "is_gone": false,
      "is_undeletable": false,
      "user": {
        "username": "jsavigny",
        "id": 514,
        "karma": 2
      },
      "tags": [
        {
          "tag": "Gadget",
          "description": "All about gadget!"
        }
      ]
    },
    {
      "id": 46,
      "title": "Tes ios fcm",
      "url": "http://komunitas.staging.vm:5000/s/bx1h6k/tes_ios_fcm",
      "created_at": "2016-08-12T09:12:21.000+07:00",
      "updated_at": "2016-08-12T09:12:21.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": null,
      "comments_count": 5,
      "is_sticky": false,
      "is_editable": false,
      "is_gone": false,
      "is_undeletable": false,
      "user": {
        "username": "jsavigny",
        "id": 514,
        "karma": 2
      },
      "tags": [
        {
          "tag": "Gadget",
          "description": "All about gadget!"
        }
      ]
    },
    {
      "id": 44,
      "title": "Markeddown",
      "url": "http://komunitas.staging.vm:5000/s/xzowv6/markeddown",
      "created_at": "2016-08-11T20:46:28.000+07:00",
      "updated_at": "2016-08-11T23:05:20.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": null,
      "comments_count": 0,
      "is_sticky": false,
      "is_editable": false,
      "is_gone": false,
      "is_undeletable": false,
      "user": {
        "username": "ragapinilih",
        "id": 1,
        "karma": 2
      },
      "tags": [
        {
          "tag": "Pengumuman",
          "description": "Pengumuman dan pemberitahuan resmi dari tim Bukalapak"
        },
        {
          "tag": "belanja",
          "description": "Curabitur turpis. Aenean leo ligula, porttitor eu, consequat vitae, eleifend ac, enim. Nulla neque dolor, sagittis eget, iaculis quis, molestie non, velit. Donec orci lectus, aliquam ut, faucibus non, euismod id, nulla. Ut a nisl id ante tempus hendrerit."
        }
      ]
    },
    {
      "id": 43,
      "title": "Topik Mention FCM",
      "url": "http://komunitas.staging.vm:5000/s/bqygkp/topik_mention_fcm",
      "created_at": "2016-08-11T19:33:10.000+07:00",
      "updated_at": "2016-08-11T19:33:10.000+07:00",
      "upvotes": 2,
      "downvotes": 0,
      "vote": null,
      "comments_count": 7,
      "is_sticky": false,
      "is_editable": false,
      "is_gone": false,
      "is_undeletable": false,
      "user": {
        "username": "jsavigny",
        "id": 514,
        "karma": 2
      },
      "tags": [
        {
          "tag": "Komputer",
          "description": "Berbagi seputar dunia komputer, laptop, dan turunannya."
        }
      ]
    },
    {
      "id": 41,
      "title": "Tifani",
      "url": "http://komunitas.staging.vm:5000/s/qcxrw5/tifani",
      "created_at": "2016-08-11T16:49:10.000+07:00",
      "updated_at": "2016-08-11T16:49:10.000+07:00",
      "upvotes": 0,
      "downvotes": 0,
      "vote": null,
      "comments_count": 0,
      "is_sticky": false,
      "is_editable": false,
      "is_gone": false,
      "is_undeletable": false,
      "user": {
        "username": "ragapinilih",
        "id": 1,
        "karma": 2
      },
      "tags": [
        {
          "tag": "Pengumuman",
          "description": "Pengumuman dan pemberitahuan resmi dari tim Bukalapak"
        }
      ]
    }
  ],
  "sticky_topics": [
    {
      "id": 19,
      "title": "Masih Ada Aja Pembeli Yang Marah-Marah di Forum Komunitas Gara-Gara Barang Belum Nyampai",
      "url": "http://komunitas.staging.vm:5000/s/qxeavi/masih_ada_aja_pembeli_yang_marah-marah_di_forum_komunitas_gara-gara_barang_belum_nyampai",
      "created_at": "2016-08-11T10:04:46.000+07:00",
      "updated_at": "2016-08-12T08:41:14.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": null,
      "comments_count": 3,
      "is_sticky": true,
      "is_editable": false,
      "is_gone": false,
      "is_undeletable": false,
      "user": {
        "username": "jsavigny",
        "id": 514,
        "karma": 2
      },
      "tags": [
        {
          "tag": "Berita",
          "description": "Berbagi informasi terbaru yang sedang hangat-hangatnya"
        },
        {
          "tag": "Inspirasi Wirausaha",
          "description": "Cerita, pengalaman, atau artikel yang memotivasi dan menginspirasi kita semua"
        }
      ]
    },
    {
      "id": 17,
      "title": "Ini Dia Pemenang Kontes Menulis Serunya Kopdar Bareng Komunitas Bukalapak (Periode Juli)",
      "url": "http://komunitas.staging.vm:5000/s/q2sran/ini_dia_pemenang_kontes_menulis_serunya_kopdar_bareng_komunitas_bukalapak_periode_juli",
      "created_at": "2016-08-11T10:00:10.000+07:00",
      "updated_at": "2016-08-11T10:00:57.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": null,
      "comments_count": 1,
      "is_sticky": true,
      "is_editable": false,
      "is_gone": false,
      "is_undeletable": false,
      "user": {
        "username": "ragapinilih",
        "id": 1,
        "karma": 2
      },
      "tags": [
        {
          "tag": "Pengumuman",
          "description": "Pengumuman dan pemberitahuan resmi dari tim Bukalapak"
        }
      ]
    },
    {
      "id": 16,
      "title": "Jawara Kontes Menulis Tips & Trik Jualan - Periode 1-7 Agustus 2016",
      "url": "http://komunitas.staging.vm:5000/s/osbtna/jawara_kontes_menulis_tips_trik_jualan_-_periode_1-7_agustus_2016",
      "created_at": "2016-08-11T09:59:12.000+07:00",
      "updated_at": "2016-08-11T09:59:16.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": null,
      "comments_count": 0,
      "is_sticky": true,
      "is_editable": false,
      "is_gone": false,
      "is_undeletable": false,
      "user": {
        "username": "ragapinilih",
        "id": 1,
        "karma": 2
      },
      "tags": [
        {
          "tag": "Pengumuman",
          "description": "Pengumuman dan pemberitahuan resmi dari tim Bukalapak"
        }
      ]
    },
    {
      "id": 15,
      "title": "[Undangan] Kopdar BL Komunitas Palembang. BEDAH LAPAK: KIAT KIAT MEMAKSIMALKAN LAPAK ANDA",
      "url": "http://komunitas.staging.vm:5000/s/aeezfl/undangan_kopdar_bl_komunitas_palembang_bedah_lapak_kiat_kiat_memaksimalkan_lapak_anda",
      "created_at": "2016-08-11T09:58:35.000+07:00",
      "updated_at": "2016-08-11T09:58:37.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": null,
      "comments_count": 2,
      "is_sticky": true,
      "is_editable": false,
      "is_gone": false,
      "is_undeletable": false,
      "user": {
        "username": "ragapinilih",
        "id": 1,
        "karma": 2
      },
      "tags": [
        {
          "tag": "Berita",
          "description": "Berbagi informasi terbaru yang sedang hangat-hangatnya"
        },
        {
          "tag": "Event",
          "description": "tentang event komunitas Bukalapak"
        }
      ]
    },
    {
      "id": 14,
      "title": "Riwayat Pemotongan Budget Promoted Push Tidak Informatif?",
      "url": "http://komunitas.staging.vm:5000/s/joiihe/riwayat_pemotongan_budget_promoted_push_tidak_informatif",
      "created_at": "2016-08-11T09:57:31.000+07:00",
      "updated_at": "2016-08-11T09:57:34.000+07:00",
      "upvotes": 1,
      "downvotes": 0,
      "vote": null,
      "comments_count": 5,
      "is_sticky": true,
      "is_editable": false,
      "is_gone": false,
      "is_undeletable": false,
      "user": {
        "username": "ragapinilih",
        "id": 1,
        "karma": 2
      },
      "tags": [
        {
          "tag": "Tips & Trik Jualan",
          "description": "Tips & Trik Jualan Online"
        }
      ]
    }
  ],
  "message": "Recent Topics"
}
```


This endpoint retrieves all topics, sticky and non sticky alike, sorted by trending or recency.

### HTTP Request

`GET http://api.bukalapak.com/komunitas/topics `

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
`tag` | 'Semua' | The tag to filter the topics.
`filter` | - | If filter = recent,then the response will return topics sorted by recency (recent topics), else sorted by trending (trending topics)
`page` | - | Pagination, each page will return 8 topics

## Get a Specific Topic

> Sample Request

```ruby
GET komunitas/topics/15
Host: api.bukalapak.com
```

```shell
curl "http://api.bukalapak.com/komunitas/topics/15"
```

> Sample Response

```json
{
  "status": "OK",
  "topic": {
    "description": "Kopdar Komunitas BL Palembang\r\n\r\nTopik: Bedah Lapak: Kiat2 memaksimalkan penggunaan lapak Anda\r\n\r\nWaktu: 14 Agustus 2016, Jam 3.30 Sore\r\n\r\nTempat: Bimbel dolphin Cb3\r\n\r\nJl. Sultan M Mansyur No. 7\r\n\r\nBukit siguntang\r\n\r\nCP: Halim 081918801525. Yadi 089622222011",
    "markeddown_description": "<p>Kopdar Komunitas BL Palembang</p>\n\n<p>Topik: Bedah Lapak: Kiat2 memaksimalkan penggunaan lapak Anda</p>\n\n<p>Waktu: 14 Agustus 2016, Jam 3.30 Sore</p>\n\n<p>Tempat: Bimbel dolphin Cb3</p>\n\n<p>Jl. Sultan M Mansyur No. 7</p>\n\n<p>Bukit siguntang</p>\n\n<p>CP: Halim 081918801525. Yadi 089622222011</p>\n",
    "id": 15,
    "title": "[Undangan] Kopdar BL Komunitas Palembang. BEDAH LAPAK: KIAT KIAT MEMAKSIMALKAN LAPAK ANDA",
    "url": "http://komunitas.staging.vm:5000/s/aeezfl/undangan_kopdar_bl_komunitas_palembang_bedah_lapak_kiat_kiat_memaksimalkan_lapak_anda",
    "created_at": "2016-08-11T09:58:35.000+07:00",
    "updated_at": "2016-08-11T09:58:37.000+07:00",
    "upvotes": 1,
    "downvotes": 0,
    "vote": null,
    "can_downvote": null,
    "comments_count": 2,
    "is_editable": false,
    "is_gone": false,
    "is_undeletable": false,
    "is_sticky": true,
    "user": {
      "username": "ragapinilih",
      "id": 1,
      "karma": 2
    },
    "tags": [
      {
        "tag": "Berita",
        "description": "Berbagi informasi terbaru yang sedang hangat-hangatnya"
      },
      {
        "tag": "Event",
        "description": "tentang event komunitas Bukalapak"
      }
    ]
  },
  "comments": [
    {
      "id": 127,
      "comment": "@juliosavigny",
      "markeddown_comment": "<p><a href=\"/u/juliosavigny\">@juliosavigny</a></p>\n",
      "upvotes": 1,
      "downvotes": 0,
      "vote": null,
      "can_downvote": null,
      "created_at": "2016-08-12T09:22:46.000+07:00",
      "updated_at": "2016-08-12T09:22:46.000+07:00",
      "parent_comment_id": null,
      "is_editable": false,
      "is_deletable": false,
      "is_undeletable": false,
      "is_gone": false,
      "user": {
        "username": "ragapinilih",
        "id": 1,
        "karma": 2,
        "avatar": "http://www.staging.vm:5000/system4/avatars/8/small/UjU1ts0_.jpg"
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

<aside class="notice">vote and can_downvote attribute is determined by the Authentication</aside>

<aside class="notice">if vote = -1, the user has already downvoted,
if vote = 1, the user has already upvoted,
if vote = null, the user hasn't voted yet
if vote = 0, then the topic is hidden from the user.</aside>

<aside class="notice">if can_downvote is true, then the user can downvote the post,
else, hide the downvote arrow</aside>

### HTTP Request

`GET http://api.bukalapak.com/komunitas/topics/:id`

### URL Parameters

Parameter | Description
--------- | -----------
`:id` | The ID of the topic to retrieve

## Create a topic

> Sample Request

```ruby
POST komunitas/topics
Host: api.bukalapak.com
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
curl -X POST "api.bukalapak.com/komunitas/topics"
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

`POST http://api.bukalapak.com/komunitas/topics/`

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
Host: api.bukalapak.com
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
curl -X POST "api.bukalapak.com/komunitas/topics"
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

`POST http://api.bukalapak.com/komunitas/topics/`

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
Host: api.bukalapak.com
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
curl -X PATCH "api.bukalapak.com/komunitas/topics/1"
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

`PATCH http://api.bukalapak.com/komunitas/topics/:id`

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
PATCH komunitas/topics/1/deletion
Host: api.bukalapak.com
Authorization: Basic user_id:api_token
```

```json
{
    "moderation_reason": "reason"
}
```

```shell
curl -X PATCH "api.bukalapak.com/komunitas/topics/1/deletion"
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

`PATCH http://api.bukalapak.com/komunitas/topics/:id/deletion`

### URL Parameters

Parameter |        |Description
--------- | -------- |-----------
`:id` | required |id of the topic
`moderation_reason` |  | reason for deletion

## Undelete a topic

> Sample Request

```ruby
PATCH komunitas/topics/1/restoration
Host: api.bukalapak.com
Authorization: Basic user_id:api_token
```

```shell
curl -X PATCH "api.bukalapak.com/komunitas/topics/1/restoration"
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

`PATCH http://api.bukalapak.com/komunitas/topics/:id/restoration`

### URL Parameters

Parameter |        |Description
--------- | -------- |-----------
`:id` | required |id of the topic


## Upvote a topic

> Sample Request

```ruby
POST komunitas/topics/1/upvotes
Host: api.bukalapak.com
Authorization: Basic user_id:api_token
```

```shell
curl -X POST "api.bukalapak.com/komunitas/topics/1/upvotes"
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

`POST http://api.bukalapak.com/komunitas/topics/:id/upvotes`

### URL Parameters

Parameter |        |Description
--------- | -------- |-----------
`:id` | required |id of the topic

## Downvote a topic

> Sample Request

```ruby
POST komunitas/topics/1/downvotes
Host: api.bukalapak.com
Authorization: Basic user_id:api_token
```

```json
{
  "reason":"O"
}
```

```shell
curl -X POST "api.bukalapak.com/komunitas/topics/1/downvotes"
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

`POST http://api.bukalapak.com/komunitas/topics/:id/downvotes`

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
Host: api.bukalapak.com
Authorization: Basic user_id:api_token
```

```shell
curl -X POST "api.bukalapak.com/komunitas/topics/1/unvotes"
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

`POST http://api.bukalapak.com/komunitas/topics/:id/unvotes`

### URL Parameters

Parameter |        |Description
--------- | -------- |-----------
`:id` | required |id of the topic

## Sticky / Unsticky a topic

> Sample Request

```ruby
POST komunitas/topics/1/sticky
Host: api.bukalapak.com
Authorization: Basic user_id:api_token
```

```shell
curl -X POST "api.bukalapak.com/komunitas/topics/1/sticky"
      -u "1:RnLxZ69SP0tOmJoulmG7"
```
> Sticky Success Response

```json
{
  "status": "OK",
  "message": "Sticky Success"
}
```

> Unsticky Success Response

```json
{
  "status": "OK",
  "message": "Unsticky Success"
}
```

> Authentication Error

```json
{
  "status": "ERROR",
  "message": "Anda harus login untuk mengakses halaman ini"
}
```

> Unauthorized Error

```json
{
  "status": "ERROR",
  "message": "Anda tidak dapat mengakses halaman tersebut"
}
```

This endpoint is used to make a topic a sticky one if it has not already been.
If the topic is already a sticky topic, then this action will remove the sticky status (unsticky).
Only moderators and administrators can do this action.
<aside class="notice"> Requires Authentication </aside>


### HTTP Request

`POST http://api.bukalapak.com/komunitas/topics/:id/sticky`

### URL Parameters

Parameter |        |Description
--------- | -------- |-----------
`:id` | required |id of the topic

## Hide a topic

> Sample Request

```ruby
POST komunitas/topics/1/hiding
Host: api.bukalapak.com
Authorization: Basic user_id:api_token
```

```shell
curl -X POST "api.bukalapak.com/komunitas/topics/1/hiding"
      -u "1:RnLxZ69SP0tOmJoulmG7"
```
> Hide Success Response

```json
{
  "status": "OK",
  "message": "Topic Hidden"
}
```

> Authentication Error

```json
{
  "status": "ERROR",
  "message": "Anda harus login untuk mengakses halaman ini"
}
```

> Unauthorized Error

```json
{
  "status": "ERROR",
  "message": "Anda tidak dapat mengakses halaman tersebut"
}
```

This endpoint is used to hide a topic for the current user.
<aside class="notice"> Requires Authentication </aside>


### HTTP Request

`POST http://api.bukalapak.com/komunitas/topics/:id/hiding`

### URL Parameters

Parameter |        |Description
--------- | -------- |-----------
`:id` | required |id of the topic

## Unhide a topic

> Sample Request

```ruby
DELETE komunitas/topics/1/hiding
Host: api.bukalapak.com
Authorization: Basic user_id:api_token
```

```shell
curl -X DELETE "api.bukalapak.com/komunitas/topics/1/hiding"
      -u "1:RnLxZ69SP0tOmJoulmG7"
```
> Unide Success Response

```json
{
  "status": "OK",
  "message": "Topic Unhidden"
}
```

> Authentication Error

```json
{
  "status": "ERROR",
  "message": "Anda harus login untuk mengakses halaman ini"
}
```

> Unauthorized Error

```json
{
  "status": "ERROR",
  "message": "Anda tidak dapat mengakses halaman tersebut"
}
```

This endpoint is used to unhide a hidden topic for the current user.
<aside class="notice"> Requires Authentication </aside>


### HTTP Request

`DELETE http://api.bukalapak.com/komunitas/topics/:id/hiding`

### URL Parameters

Parameter |        |Description
--------- | -------- |-----------
`:id` | required |id of the topic
