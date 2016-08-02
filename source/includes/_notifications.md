# Notifications

## Add Firebase Device

> Sample Request

```ruby
POST komunitas/notifications/firebase
Host: api.local.host:5000
Authorization: Basic user_id:api_token
```

```json
{
  "token":"f0pS3cCaJu4:APA91bEzh7Nq3T9sY-j6Oh4ttxgim-9dZS6_97isUWnrhAVxHct3nT3iyy-Kb7Ka4JjGVD3Ha6BzE9awd3M5m2Fnz5Io_cimIkyJEWdHgTtVjGoGsGcV_mUIjjae__RCgjZZ_2CZcZEj"
}
```

```shell
curl -X POST "http://api.local.host:5000/komunitas/notifications/firebase"
      -u "1:RnLxZ69SP0tOmJoulmG7"
      -d "{
            "token":"f0pS3cCaJu4:APA91bEzh7Nq3T9sY-j6Oh4ttxgim-9dZS6_97isUWnrhAVxHct3nT3iyy-Kb7Ka4JjGVD3Ha6BzE9awd3M5m2Fnz5Io_cimIkyJEWdHgTtVjGoGsGcV_mUIjjae__RCgjZZ_2CZcZEj"
          }"
```

> Sample Response


```json
{
  "status": "OK",
  "message": "Device ditambahkan"
}
```

> Failure Response

```json
{
  "status": "ERROR",
  "message": "Gagal menambahkan device"
}
```


Add user's firebase device

<aside class="notice"> Requires Authentication </aside>

### HTTP Request

`POST http://api.local.host:5000/komunitas/notifications/firebase`

### URL Parameters

Parameter |        |Description
--------- | -------- |-----------
`token` | required | registration token of the device


## Logout Firebase Device

> Sample Request

```ruby
DELETE komunitas/notifications/firebase/logout
Host: api.local.host:5000
Authorization: Basic user_id:api_token
```

```json
{
  "token":"f0pS3cCaJu4:APA91bEzh7Nq3T9sY-j6Oh4ttxgim-9dZS6_97isUWnrhAVxHct3nT3iyy-Kb7Ka4JjGVD3Ha6BzE9awd3M5m2Fnz5Io_cimIkyJEWdHgTtVjGoGsGcV_mUIjjae__RCgjZZ_2CZcZEj"
}
```

```shell
curl -X PATCH "http://api.local.host:5000/komunitas/notifications/firebase/logout"
      -u "1:RnLxZ69SP0tOmJoulmG7"
      -d "{
            "token":"f0pS3cCaJu4:APA91bEzh7Nq3T9sY-j6Oh4ttxgim-9dZS6_97isUWnrhAVxHct3nT3iyy-Kb7Ka4JjGVD3Ha6BzE9awd3M5m2Fnz5Io_cimIkyJEWdHgTtVjGoGsGcV_mUIjjae__RCgjZZ_2CZcZEj"
          }"
```

> Sample Response


```json
{
  "status": "OK",
  "message": "Device telah log out"
}
```

> Failure Response

```json
{
  "status": "ERROR",
  "message": "Gagal log out"
}
```

Logout current user from current device.
<aside class="notice"> Requires Authentication </aside>

### HTTP Request

`POST http://api.local.host:5000/komunitas/notifications/firebase`

### URL Parameters

Parameter |        |Description
--------- | -------- |-----------
`token` | required | registration token of the device
