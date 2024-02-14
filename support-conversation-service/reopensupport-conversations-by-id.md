# ReOpenSupport Conversations by id

### GET /v1/support/conversation/reopen/:id <a href="#top" id="top"></a>

Allows the support user to re-open support conversation by id on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a support user request to re-open support conversation by conversation id.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/support/conversation/reopen/:id
```

#### &#x20;**Sample request headers** <a href="#top" id="top"></a>

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

<table><thead><tr><th width="142">Key</th><th width="131">Value</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>&#x3C;id></td><td>The unique ID of the support conversation.</td></tr></tbody></table>

#### Support Conversation Object

Contains information about ZAP's platform Support Conversations.

This object is used by the following operations:

* #### POST /v1/support/conversations
* #### GET /v1/support/:userId/conversations
* #### GET /v1/support/conversation/:Id
* #### GET  /v1/support/conversation/:Id/close
* #### PUT  /v1/support/conversation/:Id

The properties included in the Support Conversation object are listed below.&#x20;

<table><thead><tr><th>Property</th><th width="141">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td>The support conversation unique ID. </td></tr><tr><td>messages</td><td>array</td><td>The field takes the array of the details of the support messages.</td></tr><tr><td>supportId</td><td>object</td><td>The details of the support user on the platform.</td></tr><tr><td>userId</td><td>object</td><td>The details of the  user who created the support conversation on the platform.</td></tr><tr><td>userUnreadCount</td><td>number</td><td>The number of unread messages sent by a user</td></tr><tr><td>supportUnreadCount</td><td>number</td><td>The number of unread messages sent by a support user</td></tr><tr><td>isClosed</td><td>boolean</td><td>The (open or closed) status of the support conversation.</td></tr><tr><td>isDeleted</td><td>boolean</td><td>The deleted status if the support conversation  is deleted.</td></tr><tr><td>deletedAt</td><td>dateTime</td><td>This field shows when the support conversation was deleted. Used only in response messages.</td></tr><tr><td>createdAt</td><td>dateTime</td><td>This property displays when the support conversation was created. Used only in response messages.</td></tr><tr><td>updatedAt</td><td>dateTime</td><td>This property displays when the support conversation was last updated. Used only in response messages.</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the closed support conversation.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Thur, 20 Jul 2023 12:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
      "success": true,
      "data": {
              "messages": [],
              "supportId": "644a53ed9829e85215296ee6",
              "userId": "644a53e99829e85215296edf",
              "userUnreadCount": 0,
              "supportUnreadCount": 0,
              "isClosed": false,
              "createdAt": "2023-07-20T12:14:27.089Z",
              "updatedAt": "2023-07-20T12:14:27.089Z",
              "id": "644a53f19829e85215296ef2"
          }
    }
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name                 | Type                 | Description                                                                  |
| -------------------- | -------------------- | ---------------------------------------------------------------------------- |
| Support Conversation | Support Conversation | Contains information about the closed Support Conversation on ZAP  platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |

