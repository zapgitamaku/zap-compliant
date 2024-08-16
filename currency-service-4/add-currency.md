# Create Support Command

### POST /v1/supportCommand <a href="#top" id="top"></a>

Allows the zap support user to Create a new support command on the platform.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to Create a new support command

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/supportCommand
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
    "command": "/hello",
    "message": "hello"
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                              |
| Authorization | This is the ZAP API Platform authorization token, and must be sent with every API request that requires login |

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="200">Parameter</th><th width="98">Parm Type</th><th width="101">Required</th><th>Description</th></tr></thead><tbody><tr><td>SupportCommand</td><td>Body</td><td>Required</td><td>Contains information about auto messages on ZAP platform name and userId, message and command are required.</td></tr></tbody></table>

#### SupportCommand Object

Contains information about ZAP's platform support command.

The properties included in the SupportCommand object are listed below. All property are **Required**.

<table><thead><tr><th>Property</th><th width="150">Type</th><th>Description</th></tr></thead><tbody><tr><td>userId</td><td>string</td><td>The unique ID for a specific support user.</td></tr><tr><td>message</td><td>string</td><td>The message of the command.</td></tr><tr><td>command</td><td>string</td><td>The name of the command</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 201, with information about the new support command.

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
            "command": "/hello",
            "message": "hello",
            "createdAt": "2024-05-06T15:27:33.310Z",
            "updatedAt": "2024-05-06T15:27:33.310Z",
            "id": "6638f6e50ac96302de75c94b"
        }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name           | Type           | Description                                                 |
| -------------- | -------------- | ----------------------------------------------------------- |
| SupportCommand | SupportCommand | Contains information about support command on ZAP platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |
