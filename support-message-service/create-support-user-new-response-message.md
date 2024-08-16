# Create Support User New Response Message

### POST /v1/support/response/messages <a href="#top" id="top"></a>

Allows the support user to create a new response support message in a conversation on the platform.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a support user request to Create a new response support message in a conversation.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/support/response/messages
```

#### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

#### **Sample request body** <a href="#top" id="top"></a>

<pre class="language-json"><code class="lang-json">{    
<strong>    "userId": "647df18a05647ed1d5193ba8",
</strong>    "message": "Hi, Support.",
    "messageHtml": "&#x3C;div>Hi, Support&#x3C;/div.",
    "fileType": "",
    // "fileUrl": "",
    "conversationId": "660699486386958b44c2550b"
};
</code></pre>

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                              |
| Authorization | This is the ZAP API Platform authorization token, and must be sent with every API request that requires login |

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="142">Parameter</th><th width="91">Parm Type</th><th width="101">Required</th><th>Description</th></tr></thead><tbody><tr><td>Support Message</td><td>Body</td><td>Required</td><td>Contains information about creating support messages on ZAP platform. userId, message and conversationId is required, and fileUrl and fileType is optional.</td></tr></tbody></table>

#### Support Message Object

Contains information about ZAP's platform Support Messages.

This object is used by the following operations:

* **POST /v1/support/messages**
* **POST /v1/support/response/messages**
* **GET /v1/support/:conversationId/messages**
* **GET /v1/support/messages/:Id**
* **PUT /v1/support/messages/:Id**

The properties included in the Support Conversation object are listed below.

<table><thead><tr><th>Property</th><th width="141">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td>The support message unique ID.</td></tr><tr><td>messages</td><td>string</td><td>The field takes the message sent.</td></tr><tr><td>conversationId</td><td>string</td><td>The unique ID of the support conversation opened for the support messages to be sent on the platform.</td></tr><tr><td>userId</td><td>string</td><td>The unique ID of the user who sent the support message on the platform.</td></tr><tr><td>fileUrl</td><td>string</td><td>The url of the file sent.</td></tr><tr><td>fileType</td><td>string</td><td>The type of the file sent.</td></tr><tr><td>messageHtml</td><td>string</td><td>The markdown of the message sent.</td></tr><tr><td>isDeleted</td><td>boolean</td><td>The deleted status if the support message is deleted.</td></tr><tr><td>deletedAt</td><td>dateTime</td><td>This field shows when the support message was deleted. Used only in response messages.</td></tr><tr><td>createdAt</td><td>dateTime</td><td>This property displays when the support message was created. Used only in response messages.</td></tr><tr><td>updatedAt</td><td>dateTime</td><td>This property displays when the support message was last updated. Used only in response messages.</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200 | 201, with information about the new support message.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Thur, 25 Apr 2023 13:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

<pre class="language-json"><code class="lang-json">{
      "success": true,
<strong>        "userId": "647df18a05647ed1d5193ba8",
</strong>        "onModel": "User",
        "message": "Hi, Support.",
        "messageHtml": "&#x3C;div>Hi, Support&#x3C;/div.",
        "fileType": "",
        "conversationId": "660699486386958b44c2550b",
        "read": false,
        "isBot": false,
        "createdAt": "2024-08-16T11:06:28.861Z",
        "updatedAt": "2024-08-16T11:06:28.861Z",
        "id": "66bf32b4705ce7dc8f606f18"
    }
  }
</code></pre>

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name            | Type            | Description                                                      |
| --------------- | --------------- | ---------------------------------------------------------------- |
| Support Message | Support Message | Contains information about sent Support Message on ZAP platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |
