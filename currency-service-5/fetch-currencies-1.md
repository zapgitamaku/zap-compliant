# Fetch Leaderboard Avatars

### GET /v1/avatar <a href="#top" id="top"></a>

Allows a user to get the available avatars for their zap loyalty program leaderboard profile on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to get all the leaderboard avatars

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/avatar
```

#### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                              |
| Authorization | This is the ZAP API Platform authorization token, and must be sent with every API request that requires login |

#### Avatar Object

Contains information about ZAP's platform Leaderboard.

<table><thead><tr><th width="240">Property</th><th width="150">Type</th><th>Description</th></tr></thead><tbody><tr><td>avatar</td><td>string</td><td>The url of the leaderboard avatar.</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the avatars.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Wed, 15 May 2024 17:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
    "success": true,
    "data": [
        {
            "avatar": "https://res.cloudinary.com/dclh3qo14/image/upload/v1716220557/Avatar_24_pc7xsb.png",
            "createdAt": "2024-05-20T17:23:52.397Z",
            "updatedAt": "2024-05-20T17:23:52.397Z",
            "id": "664b8728b2958607802d5745"
        },
        {
            "avatar": "https://res.cloudinary.com/dclh3qo14/image/upload/v1716220557/Avatar_20_gq8uml.png",
            "createdAt": "2024-05-20T17:23:45.773Z",
            "updatedAt": "2024-05-20T17:23:45.773Z",
            "id": "664b8721b2958607802d5741"
        },
        {
            "avatar": "https://res.cloudinary.com/dclh3qo14/image/upload/v1716220557/Avatar_23_orfhow.png",
            "createdAt": "2024-05-20T17:23:39.290Z",
            "updatedAt": "2024-05-20T17:23:39.290Z",
            "id": "664b871bb2958607802d573d"
        },
        {
            "avatar": "https://res.cloudinary.com/dclh3qo14/image/upload/v1716220557/Avatar_17_jz3h61.png",
            "createdAt": "2024-05-20T17:23:22.479Z",
            "updatedAt": "2024-05-20T17:23:22.479Z",
            "id": "664b870ab2958607802d5739"
        },
        {
            "avatar": "https://res.cloudinary.com/dclh3qo14/image/upload/v1716220557/Avatar_18_evusxz.png",
            "createdAt": "2024-05-20T17:23:13.936Z",
            "updatedAt": "2024-05-20T17:23:13.936Z",
            "id": "664b8701b2958607802d5735"
        },
        {
            "avatar": "https://res.cloudinary.com/dclh3qo14/image/upload/v1716220557/Avatar_21_njye2t.png",
            "createdAt": "2024-05-20T17:23:05.737Z",
            "updatedAt": "2024-05-20T17:23:05.737Z",
            "id": "664b86f9b2958607802d5731"
        },
        {
            "avatar": "https://res.cloudinary.com/dclh3qo14/image/upload/v1716220557/Avartar_13_cvuqrx.png",
            "createdAt": "2024-05-20T17:22:55.801Z",
            "updatedAt": "2024-05-20T17:22:55.801Z",
            "id": "664b86efb2958607802d572d"
        },
        {
            "avatar": "https://res.cloudinary.com/dclh3qo14/image/upload/v1716220557/Avatar_22_r8zygr.png",
            "createdAt": "2024-05-20T17:22:50.068Z",
            "updatedAt": "2024-05-20T17:22:50.068Z",
            "id": "664b86eab2958607802d5729"
        },
        {
            "avatar": "https://res.cloudinary.com/dclh3qo14/image/upload/v1716220557/Avatar_16_me3sdp.png",
            "createdAt": "2024-05-20T17:22:40.542Z",
            "updatedAt": "2024-05-20T17:22:40.542Z",
            "id": "664b86e0b2958607802d5725"
        },
        {
            "avatar": "https://res.cloudinary.com/dclh3qo14/image/upload/v1716220557/Avatar_19_ojhoxc.png",
            "createdAt": "2024-05-20T17:22:27.562Z",
            "updatedAt": "2024-05-20T17:22:27.562Z",
            "id": "664b86d3b2958607802d5721"
        },
        {
            "avatar": "https://res.cloudinary.com/dclh3qo14/image/upload/v1716220557/avatar_10_q0s19g.png",
            "createdAt": "2024-05-20T17:21:11.967Z",
            "updatedAt": "2024-05-20T17:21:11.967Z",
            "id": "664b8687b2958607802d571d"
        },
        {
            "avatar": "https://res.cloudinary.com/dclh3qo14/image/upload/v1716220558/avatar_11_kkmzi7.png",
            "createdAt": "2024-05-20T17:20:54.054Z",
            "updatedAt": "2024-05-20T17:20:54.054Z",
            "id": "664b8676b2958607802d5719"
        }
    ]
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name            | Type            | Description                                                     |
| --------------- | --------------- | --------------------------------------------------------------- |
| <h4>Avatar</h4> | <h4>Avatar</h4> | Contains information about leaderboard avatars on ZAP platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                   |
| ---- | --------------------------------------- |
| 404  | The resource could not be found.        |
| 500  | An error occured processing the request |
