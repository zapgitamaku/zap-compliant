# Create Auto Message

### POST /v1/autoMessage <a href="#top" id="top"></a>

Allows the zap support user to Create a new auto message on the platform.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to Create a new auto message.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/autoMessage
```

#### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

#### **Sample request body** <a href="#top" id="top"></a>

```json
{
    "userId": "6515a38ef6d2985656496941",
    "message": "We are on a short break",
    "isActive": true
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                              |
| Authorization | This is the ZAP API Platform authorization token, and must be sent with every API request that requires login |

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="166">Parameter</th><th width="98">Parm Type</th><th width="116">Required</th><th>Description</th></tr></thead><tbody><tr><td>AutoMessage</td><td>Body</td><td>Required</td><td>Contains information about auto messages on ZAP platform name and userId, message and isActive are required.</td></tr></tbody></table>

#### AutoMessage Object

Contains information about ZAP's platform auto messages.

The properties included in the AutoMessage object are listed below. All property are **Required**.

<table><thead><tr><th>Property</th><th width="150">Type</th><th>Description</th></tr></thead><tbody><tr><td>userId</td><td>string</td><td>The unique ID for a specific support user.</td></tr><tr><td>message</td><td>string</td><td>The auto message.</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 201, with information about the new auto message.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 201 OK
Date: Wed, 15 Apr 2024 23:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
    "success": true,
    "data": {
        "userId": "6515a38ef6d2985656496941",
        "message": "We are on a short break",
        "status": "on",
        "createdAt": "2024-04-16T11:12:19.503Z",
        "updatedAt": "2024-04-16T11:12:19.503Z",
        "id": "661e5d131b55cdb434f1df12"
    }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name        | Type        | Description                                               |
| ----------- | ----------- | --------------------------------------------------------- |
| AutoMessage | AutoMessage | Contains information about auto messages on ZAP platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |
