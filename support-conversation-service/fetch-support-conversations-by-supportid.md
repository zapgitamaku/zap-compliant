# Fetch Support Conversations by supportId

### GET /v1/support/conversations/supportId <a href="#top" id="top"></a>

Allows the support user to get all their support conversations and conversations with no support user response yet on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a support user request to get all their support conversations.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/support/conversations/supportId
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

This endpoint takes no parameters as it get the support user id and roleId (for permission to access the endpoint) from the authorization token

#### Support Conversation Object

Contains information about ZAP's platform Support Conversations.

This object is used by the following operations:

* **POST /v1/support/conversations**
* **GET /v1/support/:userId/conversations**
* **GET /v1/support/conversations/supportId**
* **GET /v1/support/conversation/:Id**
* **GET /v1/support/conversation/:Id/close**
* **PUT /v1/support/conversation/:Id**

The properties included in the Support Conversation object are listed below.

<table><thead><tr><th>Property</th><th width="141">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td>The support conversation unique ID.</td></tr><tr><td>messages</td><td>array</td><td>The field takes the array of the details of the support messages.</td></tr><tr><td>supportId</td><td>object</td><td>The details of the support user on the platform.</td></tr><tr><td>userId</td><td>object</td><td>The details of the user who created the support conversation on the platform.</td></tr><tr><td>userUnreadCount</td><td>number</td><td>The number of unread messages sent by a user</td></tr><tr><td>supportUnreadCount</td><td>number</td><td>The number of unread messages sent by a support user</td></tr><tr><td>isClosed</td><td>boolean</td><td>The (open or closed) status of the support conversation.</td></tr><tr><td>isDeleted</td><td>boolean</td><td>The deleted status if the support conversation is deleted.</td></tr><tr><td>deletedAt</td><td>dateTime</td><td>This field shows when the support conversation was deleted. Used only in response messages.</td></tr><tr><td>createdAt</td><td>dateTime</td><td>This property displays when the support conversation was created. Used only in response messages.</td></tr><tr><td>updatedAt</td><td>dateTime</td><td>This property displays when the support conversation was last updated. Used only in response messages.</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the support conversations.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Thur, 01 Jun 2023 13:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
    "success": true,
    "data": [
    {
        "type": "Chat",
        "escalatedAt": null,
        "reviewedAt": null,
        "botResponded": false,
        "messages": [
            {
                "isBot": false,
                "userId": "647f1d1e05647ed1d5195ff3",
                "onModel": "User",
                "message": "Hi hi",
                "conversationId": "6564ac56e4816a40bbebc4bb",
                "read": true,
                "createdAt": "2023-11-27T14:48:55.309Z",
                "updatedAt": "2023-11-27T14:49:14.824Z",
                "id": "6564ac57e4816a40bbebc4c8"
            },
            {
                "isBot": false,
                "userId": "64cb7a4950ed4779921162d4",
                "onModel": "User",
                "message": "hi",
                "fileUrl": "",
                "fileType": "",
                "conversationId": "6564ac56e4816a40bbebc4bb",
                "read": true,
                "createdAt": "2023-11-27T14:49:17.827Z",
                "updatedAt": "2023-11-27T14:49:18.975Z",
                "id": "6564ac6de4816a40bbebc515"
            },
            {
                "isBot": false,
                "userId": "647f1d1e05647ed1d5195ff3",
                "onModel": "User",
                "message": "Okay ",
                "fileUrl": "",
                "fileType": "",
                "conversationId": "6564ac56e4816a40bbebc4bb",
                "read": true,
                "createdAt": "2023-11-27T14:53:19.171Z",
                "updatedAt": "2023-11-27T16:16:08.093Z",
                "id": "6564ad5fe4816a40bbebc60f"
            },
            {
                "isBot": false,
                "userId": "64cb7a4950ed4779921162d4",
                "onModel": "User",
                "message": "hi zapper",
                "fileUrl": "",
                "fileType": "",
                "conversationId": "6564ac56e4816a40bbebc4bb",
                "read": true,
                "createdAt": "2023-11-28T10:09:02.768Z",
                "updatedAt": "2023-11-28T10:09:04.391Z",
                "id": "6565bc3e8068dd0a8aacd477"
            },
            {
                "isBot": false,
                "userId": "64cb7a4950ed4779921162d4",
                "onModel": "User",
                "message": "this is a test",
                "fileUrl": "",
                "fileType": "",
                "conversationId": "6564ac56e4816a40bbebc4bb",
                "read": true,
                "createdAt": "2023-11-28T10:09:06.162Z",
                "updatedAt": "2023-11-28T10:09:07.901Z",
                "id": "6565bc428068dd0a8aacd492"
            },
            {
                "isBot": false,
                "userId": "64cb7a4950ed4779921162d4",
                "onModel": "User",
                "message": "acknowledge",
                "fileUrl": "",
                "fileType": "",
                "conversationId": "6564ac56e4816a40bbebc4bb",
                "read": true,
                "createdAt": "2023-11-28T10:09:46.408Z",
                "updatedAt": "2023-11-28T10:09:48.016Z",
                "id": "6565bc6a8068dd0a8aacd4b4"
            }
        ],
        "supportId": {
            "name": "Chuks Okwus",
            "email": "chukwuma+support@syxlabs.com",
            "username": "CO2",
            "deviceToken": [
                "fCXoPYZezUN9kn3PJyNsX3:APA91bEG-MWS8BuXjdVx5HWT0Mf3P7iVAB2-mZ5O2xMLbc7NbgMgYMWPLZarud5V8Xe3vCosIOYna7Mg8ey1j1RMJ9RyZLzHNSV-NHVnl-SeGc3W-um2bTRu8mAhMpTj0XA_kkrhchLA",
                "e0pBZAHTYUPUgHpr3L3Y1p:APA91bEc_Ajij9whGHjFfClS3AsShzgWPHYvPC_Z4Wc-O1bPX2YLUg6g2HJxKupvwoAVa0sqXf9QePTymudRKYItTc29PI0Xj5SeIWbFDXtffrWIbzHeZuiQ3s01qVdAaGA26Ek-aisS",
                "ctw9A0BccU39ltojGmd9Lw:APA91bFVUcaEGy5D4mcXZr-n7mVY7T-HGiePdzVBx4x9VkGjOuNYyne8nifLJpsXaRmzR9ZJC1JvJstllTjqheRpzGRWIDySSEc3XokWJpxlKUPIL-KRfZoSOGkJgTGHOf9lxGPwV1ic"
            ],
            "id": "64cb7a4950ed4779921162d4"
        },
        "userId": {
            "name": "Chukwuma Okwuanalu",
            "email": "chukwuma@syxlabs.com",
            "username": "chukwuma1",
            "transactionVolume": 158.31557858775403,
            "isAffiliate": true,
            "deviceToken": [
                "cIX67OJ_DEqSuQjdwvyr3Z:APA91bF9kTvPkYQy_awDvI66nwU5NRoxqarqDlyr0X7uopOeGCTBTDRokdF2gq9dYdj1w0rj2vAILYgeD6fSs55Y4ZaPn_hqCXNv8c9ubkxg4JhlOH14Yas3plK6GfgDjZLO8eVcoWw_"
            ],
            "id": "647f1d1e05647ed1d5195ff3"
        },
        "onModel": "User",
        "userUnreadCount": 0,
        "supportUnreadCount": 0,
        "isClosed": true,
        "createdAt": "2023-11-27T14:48:54.145Z",
        "updatedAt": "2024-07-03T18:55:06.009Z",
        "rating": 4,
        "isEscalated": false,
        "closedAt": "2023-11-28T10:22:55.673Z",
        "id": "6564ac56e4816a40bbebc4bb"
        }
    ]
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name                 | Type                 | Description                                                      |
| -------------------- | -------------------- | ---------------------------------------------------------------- |
| Support Conversation | Support Conversation | Contains information about Support Conversation on ZAP platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |
