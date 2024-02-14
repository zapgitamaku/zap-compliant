# Add Conversation Rating

### PUT /v1/support/conversation/rating/:id <a href="#top" id="top"></a>

Allows a zap user and guest to give rating about their support conversation.

#### HTTP Method <a href="#top" id="top"></a>

PUT

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request for a zap user and guest to give rating about their support conversation.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/support/conversation/rating/:id
```

### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

#### For Guests: <a href="#top" id="top"></a>

```
'guest-id: 63e0f4da81979dcc3b9ee123'
```

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="154">Key</th><th width="128">Value</th><th>Description</th></tr></thead><tbody><tr><td>Id</td><td>&#x3C;Id> </td><td>The unique ID for a conversation. make sure the guest/user making this rating is the user of the conversation. </td></tr></tbody></table>

#### &#x20;**Sample request body** <a href="#top" id="top"></a>

```json
{
    "comment": "calm and helping",
    "rating": 4
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                              |
| Authorization | This is the ZAP API Platform authorization token, and must be sent with every API request that requires login |
| guest-id      | This is the Id of the Guest                                                                                   |

## Request Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="129">Parameter</th><th width="70">Parm Type</th><th width="100">Data Type</th><th width="99">Required</th><th>Description</th></tr></thead><tbody><tr><td>Conversation</td><td>Body</td><td>Conversation</td><td>Optional</td><td>Contains information about  conversation rating.<br>rating is required and comment field is optional</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the updated order.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Wed, 25 Jan 2023 23:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
    "success": true,
    "data": {
        "messages": [
            {
                "userId": "64f723ba2d446208e536cf39",
                "onModel": "User",
                "message": "another one",
                "conversationId": "655604a24a220da7815ce5c9",
                "read": true,
                "createdAt": "2023-11-16T12:01:39.341Z",
                "updatedAt": "2023-11-16T12:01:46.784Z",
                "id": "655604a34a220da7815ce5d5"
            },
            {
                "userId": "647eeb1c05647ed1d5194f54",
                "onModel": "User",
                "message": "Yes",
                "fileUrl": "",
                "fileType": "",
                "conversationId": "655604a24a220da7815ce5c9",
                "read": true,
                "createdAt": "2023-11-16T12:01:49.874Z",
                "updatedAt": "2023-11-16T12:01:50.987Z",
                "id": "655604ad4a220da7815ce61f"
            },
            {
                "userId": "647eeb1c05647ed1d5194f54",
                "onModel": "User",
                "message": "sds",
                "fileUrl": "",
                "fileType": "",
                "conversationId": "655604a24a220da7815ce5c9",
                "read": true,
                "createdAt": "2023-11-16T12:08:40.920Z",
                "updatedAt": "2023-11-16T12:09:22.064Z",
                "id": "655606484a220da7815ced8a"
            },
            {
                "userId": "647eeb1c05647ed1d5194f54",
                "onModel": "User",
                "message": "sd",
                "fileUrl": "",
                "fileType": "",
                "conversationId": "655604a24a220da7815ce5c9",
                "read": true,
                "createdAt": "2023-11-16T12:09:16.379Z",
                "updatedAt": "2023-11-16T12:09:22.065Z",
                "id": "6556066c4a220da7815cee42"
            },
            {
                "userId": "64f723ba2d446208e536cf39",
                "onModel": "User",
                "message": "nice",
                "fileUrl": "",
                "fileType": "",
                "conversationId": "655604a24a220da7815ce5c9",
                "read": true,
                "createdAt": "2023-11-16T12:09:23.765Z",
                "updatedAt": "2023-11-16T12:09:25.996Z",
                "id": "655606734a220da7815cee91"
            }
        ],
        "supportId": {
            "name": "ZapTest Support",
            "email": "amaku+support@syxlabs.com",
            "id": "647eeb1c05647ed1d5194f54"
        },
        "userId": {
            "username": "folafunmi",
            "email": "folafunmi+1@syxlabs.com",
            "name": "Folafunmi Mustapha",
            "id": "64f723ba2d446208e536cf39"
        },
        "onModel": "User",
        "userUnreadCount": 0,
        "supportUnreadCount": 0,
        "isClosed": false,
        "createdAt": "2023-11-16T12:01:38.238Z",
        "updatedAt": "2023-11-21T13:07:40.565Z",
        "comment": "nice and fast trading",
        "rating": 5,
        "id": "655604a24a220da7815ce5c9"
    }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name         | Type         | Description                                                |
| ------------ | ------------ | ---------------------------------------------------------- |
| Conversation | Conversation | Contains information about  conversation on ZAP  platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |

