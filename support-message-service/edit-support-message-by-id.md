# Edit Support Message by id

### PUT /v1/support/messages/:id <a href="#top" id="top"></a>

Allows the user to modify a support message by id in a conversation on the platform.

#### HTTP Method <a href="#top" id="top"></a>

PUT

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a user request to modify a support message by id.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/support/messages/:id
```

#### &#x20;**Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

#### &#x20;**Sample request body** <a href="#top" id="top"></a>

```json
{
      "message": "Thanks for the help"
};
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                              |
| Authorization | This is the ZAP API Platform authorization token, and must be sent with every API request that requires login |

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="142">Parameter</th><th width="91">Parm Type</th><th width="101">Required</th><th>Description</th></tr></thead><tbody><tr><td>Support Message</td><td>Body</td><td>Optional</td><td>Contains information about creating  support messages on ZAP platform. userId, message, conversationId, fileUrl and fileType are optional.</td></tr></tbody></table>

#### Support Message Object

Contains information about ZAP's platform Support Messages.

This object is used by the following operations:

* #### POST /v1/support/conversations
* #### GET /v1/support/:conversationId/messages
* #### GET /v1/support/messages/:Id
* #### PUT  /v1/support/messages/:Id

The properties included in the Support Conversation object are listed below.&#x20;

<table><thead><tr><th>Property</th><th width="141">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td>The support message unique ID. </td></tr><tr><td>messages</td><td>string</td><td>The field takes the message sent.</td></tr><tr><td>conversationId</td><td>string</td><td>The unique ID of the support conversation opened for the support messages to be sent on the platform.</td></tr><tr><td>userId</td><td>string</td><td>The unique ID of the  user who sent the  support message on the platform.</td></tr><tr><td>fileUrl</td><td>string</td><td>The url of the file sent.</td></tr><tr><td>fileType</td><td>string</td><td>The type of the file sent.</td></tr><tr><td>isDeleted</td><td>boolean</td><td>The deleted status if the support message is deleted.</td></tr><tr><td>deletedAt</td><td>dateTime</td><td>This field shows when the support message was deleted. Used only in response messages.</td></tr><tr><td>createdAt</td><td>dateTime</td><td>This property displays when the support message was created. Used only in response messages.</td></tr><tr><td>updatedAt</td><td>dateTime</td><td>This property displays when the support message was last updated. Used only in response messages.</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the modified support message.

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
      "data": {
        "messages": "Thanks for the help",
        "conversationId": "644a9e270b803077ce269b68",
        "userId": "644a9e1f0b803077ce269b58",
        "read": false,
        "createdAt": "2023-04-27T10:52:33.039Z",
        "updatedAt": "2023-04-27T10:52:33.039Z",
        "id": "644a9e270b803077ce269b6d"
      }
    }
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name            | Type            | Description                                                        |
| --------------- | --------------- | ------------------------------------------------------------------ |
| Support Message | Support Message | Contains information about  sent Support Message on ZAP  platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |

