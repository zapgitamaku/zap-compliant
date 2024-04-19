# Fetch Auto Messages

### GET /v1/autoMessage <a href="#top" id="top"></a>

Allows a support user to get a list of auto messages on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to get a list of auto messages.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/autoMessage
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

#### AutoMessage Object

Contains information about ZAP's platform auto messages.

<table><thead><tr><th>Property</th><th width="150">Type</th><th>Description</th></tr></thead><tbody><tr><td>userId</td><td>string</td><td>The unique ID for a specific support user.</td></tr><tr><td>message</td><td>string</td><td>The auto message.</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the auto messages.

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
            "message": "We are on a short break. We will respond shortly.",
            "status": "on",
            "createdAt": "2024-04-16T11:12:19.503Z",
            "updatedAt": "2024-04-16T15:11:10.851Z",
            "id": "661e5d131b55cdb434f1df12"
        }
    ]
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

| Item | Value                                   |
| ---- | --------------------------------------- |
| 404  | The resource could not be found.        |
| 500  | An error occured processing the request |
