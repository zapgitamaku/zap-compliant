# Fetch Support Messages by conversationId

### GET /v1/support/:conversationId/messages <a href="#top" id="top"></a>

Allows the user to get all support messages of a specific support conversation by conversationId on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a user request to get all support messages of a conversation by conversationId.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/support/:conversationId/messages
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

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="163">key</th><th width="173">value</th><th>Description</th></tr></thead><tbody><tr><td>conversationId</td><td>&#x3C;conversationId></td><td>The unique ID of the support conversation opened for the support messages to be sent on the platform.</td></tr></tbody></table>

#### Support Message Object

Contains information about ZAP's platform Support Messages.

This object is used by the following operations:

* **POST /v1/support/conversations**
* **GET /v1/support/:conversationId/messages**
* **GET /v1/support/messages/:Id**
* **PUT /v1/support/messages/:Id**

The properties included in the Support Conversation object are listed below.

<table><thead><tr><th>Property</th><th width="141">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td>The support message unique ID.</td></tr><tr><td>messages</td><td>string</td><td>The field takes the message sent.</td></tr><tr><td>conversationId</td><td>string</td><td>The unique ID of the support conversation opened for the support messages to be sent on the platform.</td></tr><tr><td>userId</td><td>string</td><td>The unique ID of the user who sent the support message on the platform.</td></tr><tr><td>fileUrl</td><td>string</td><td>The url of the file sent.</td></tr><tr><td>fileType</td><td>string</td><td>The type of the file sent.</td></tr><tr><td>isDeleted</td><td>boolean</td><td>The deleted status if the support message is deleted.</td></tr><tr><td>deletedAt</td><td>dateTime</td><td>This field shows when the support message was deleted. Used only in response messages.</td></tr><tr><td>createdAt</td><td>dateTime</td><td>This property displays when the support message was created. Used only in response messages.</td></tr><tr><td>updatedAt</td><td>dateTime</td><td>This property displays when the support message was last updated. Used only in response messages.</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the support messages.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Thur, 25 Apr 2023 13:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
      "success": true,
      "data": [
         {
            "isBot": false,
            "userId": {
                "username": "az",
                "email": "azeez+1@zap.africa",
                "name": "Azeez Akande",
                "id": "656704bcb8ff0977fb0cb056"
            },
            "onModel": "User",
            "message": "Hi",
            "conversationId": "660699486386958b44c2550b",
            "read": true,
            "createdAt": "2024-03-29T10:34:49.592Z",
            "updatedAt": "2024-04-02T15:42:43.034Z",
            "id": "660699496386958b44c25517"
        },
        {
            "isBot": false,
            "userId": {
                "username": "az",
                "email": "azeez+1@zap.africa",
                "name": "Azeez Akande",
                "id": "656704bcb8ff0977fb0cb056"
            },
            "onModel": "User",
            "message": "I need help ",
            "fileUrl": "",
            "fileType": "",
            "conversationId": "660699486386958b44c2550b",
            "read": true,
            "createdAt": "2024-03-29T10:35:10.251Z",
            "updatedAt": "2024-04-02T15:42:43.052Z",
            "id": "6606995e6386958b44c25572"
        },
      ]
    }
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name            | Type            | Description                                                       |
| --------------- | --------------- | ----------------------------------------------------------------- |
| Support Message | Support Message | Contains information about sent Support Messages on ZAP platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |
