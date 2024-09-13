# Bulk Support actions(Escalate,Close, MarkAsSpam)

### POST /v1/support/conversation/bulkActions <a href="#top" id="top"></a>

Allows zap support users to handle several conversations and escalate them, close them or mark them as spam

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request for a zap user and guest to escalate their support conversation or send a review.

#### **Sample request** URL <a href="#top" id="top"></a>

{% code fullWidth="true" %}
```
https://{hostname}/v1/support/conversation/bulkActions
```
{% endcode %}

### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```



## Request Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="184">Key</th><th width="128">Value</th><th>Description</th></tr></thead><tbody><tr><td>ids</td><td>&#x3C;conversationIds>[]</td><td>The array of unique ID for a conversation. make sure the guest/user escalating the conversation is the user of the conversation.</td></tr><tr><td>reason</td><td>string</td><td>string(Required if action is Escalate)</td></tr></tbody></table>

## Request Query <a href="#samplerequest" id="samplerequest"></a>

| Key    | Value                       | Description                                  |
| ------ | --------------------------- | -------------------------------------------- |
| action | escalate, close, markAsSpam | the enum must be escalate, close, markAsSpam |

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
    "data": "successfully handled bulk conversation updates"
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |



### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |
| 401  | When the request is made to teh endpoint without authorization                                                                                                                                                                                                                                                                    |
