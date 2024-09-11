# Mark Support Conversation as spam

### POST /v1/support/conversation/:conversationId/markAsSpam <a href="#top" id="top"></a>

Allows zap support users to mark conversation as spam.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request for a zap user and guest to escalate their support conversation or send a review.

#### **Sample request** URL <a href="#top" id="top"></a>

{% code fullWidth="true" %}
```
https://{hostname}/v1/support/conversation/:conversationId/markAsSpam
```
{% endcode %}

### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```



## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="154">Key</th><th width="128">Value</th><th>Description</th></tr></thead><tbody><tr><td>conversationId</td><td>&#x3C;Id></td><td>The unique ID for a conversation. make sure the guest/user escalating the conversation is the user of the conversation.</td></tr></tbody></table>



## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                              |
| Authorization | This is the ZAP API Platform authorization token, and must be sent with every API request that requires login |



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
        "messages": [],
        "supportId": "644a53ed9829e85215296ee6",
        "userId": "644a53e99829e85215296edf",
        "userUnreadCount": 0,
        "supportUnreadCount": 0,
        "isClosed": true,
        "isSpam": true,
        "createdAt": "2023-04-27T10:52:33.039Z",
        "updatedAt": "2023-04-27T10:52:33.039Z",
        "id": "644a53f19829e85215296ef2"
      }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name         | Type         | Description                                                       |
| ------------ | ------------ | ----------------------------------------------------------------- |
| Conversation | Conversation | Contains information about conversation and user on ZAP platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |
| 401  | When the request is made to teh endpoint without authorization                                                                                                                                                                                                                                                                    |
