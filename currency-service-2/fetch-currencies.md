# Fetch Support Commands

### GET /v1/supportCommand/all <a href="#top" id="top"></a>

Allows a support user to get a list of support command on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to get a list of support commands.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/supportCommand/all
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

#### Support Command Object

Contains information about ZAP's platform support command.

<table><thead><tr><th>Property</th><th width="150">Type</th><th>Description</th></tr></thead><tbody><tr><td>userId</td><td>string</td><td>The unique ID for a specific support user.</td></tr><tr><td>message</td><td>string</td><td>The message of the command</td></tr><tr><td>command</td><td>string</td><td>The support command</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the support commands.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Wed, 15 Apr 2024 23:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
    "success": true,
    "data": [
        {
            "userId": "6515a38ef6d2985656496941",
            "command": "/hello",
            "message": "hello",
            "createdAt": "2024-05-06T15:27:33.310Z",
            "updatedAt": "2024-05-06T15:27:33.310Z",
            "id": "6638f6e50ac96302de75c94b"
        }
    ]
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name           | Type           | Description                                                  |
| -------------- | -------------- | ------------------------------------------------------------ |
| SupportCommand | SupportCommand | Contains information about support commands on ZAP platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                   |
| ---- | --------------------------------------- |
| 404  | The resource could not be found.        |
| 500  | An error occured processing the request |
