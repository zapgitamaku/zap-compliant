# Escalate Support Conversation

### PUT /v1/support/conversation/:id/notes <a href="#top" id="top"></a>

Allows a zap user and guest to escalate a support conversation or send review about their support conversation.

#### HTTP Method <a href="#top" id="top"></a>

PUT

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request for a zap user and guest to escalate their support conversation or send a review.

#### **Sample request** URL <a href="#top" id="top"></a>

{% code fullWidth="true" %}
```
https://{hostname}/v1/support/conversation/:id/notes
```
{% endcode %}

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

<table><thead><tr><th width="154">Key</th><th width="128">Value</th><th>Description</th></tr></thead><tbody><tr><td>Id</td><td>&#x3C;Id></td><td>The unique ID for a conversation. make sure the guest/user escalating the conversation is the user of the conversation.</td></tr></tbody></table>

#### **Sample request body** <a href="#top" id="top"></a>

```json
{
    "reviewType": "escalate",
    "reason": "customer's issue has taken so long"
}
```



#### Sample request body 2

```json
{
    "reviewType": "review",
    "note": "Agent ensured the issue was handled quickly"
}
```

#### Review type can either be "review" or "escalate"&#x20;

Review type "review" must have a "note" field while type "escalate" will have a "reason" field as seen above.



## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                              |
| Authorization | This is the ZAP API Platform authorization token, and must be sent with every API request that requires login |
| guest-id      | This is the Id of the Guest                                                                                   |

## Request Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="129">Parameter</th><th width="79">Parm Type</th><th width="113">Data Type</th><th width="99">Required</th><th>Description</th></tr></thead><tbody><tr><td>reviewType</td><td>Body</td><td>either "review" or "escalate"</td><td>Required</td><td>Contains information about conversation rating.<br>rating is required and comment field is optional</td></tr><tr><td>reason</td><td>Body</td><td>string</td><td>Optional</td><td>Field must be present if reviewType is "escalate" </td></tr><tr><td>notes</td><td>Body</td><td>string</td><td>Optional</td><td>Field must be present if reviewType is "review" </td></tr></tbody></table>

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
        "supportId": null,
        "userId": {
            "username": "diel343",
            "email": "nie@zap.africa",
            "isAffiliate": false,
            "transactionVolume": 0,
            "id": "668e6a911213eda92dc18232a"
        },
        "onModel": "User",
        "reviewType": "escalate",
        "userUnreadCount": 0,
        "supportUnreadCount": 0,
        "isClosed": false,
        "isEscalated": true,
        "closedAt": null,
        "escalatedAt": "2024-07-10T12:01:31.298Z",
        "reviewedAt": null,
        "botResponded": false,
        "createdAt": "2024-07-10T12:00:56.688Z",
        "updatedAt": "2024-07-10T12:01:31.299Z",
        "notes": "",
        "reason": "escalating zap is a must, everyone should use zap!",
        "id": "668e77f8323b42t2t0f6abb49"
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
