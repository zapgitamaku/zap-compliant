# Enable 2 Factor Authentication

### POST /v1/business/enable2fa/:id <a href="#top" id="top"></a>

Allows the zap business user to enable 2FA on the platform..

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to enable 2FA.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/business/enable2fa/:id
```

#### **Sample request headers** <a href="#top" id="top"></a>

```javascript
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="241">Header</th><th>Description</th></tr></thead><tbody><tr><td>Content-type</td><td>application/json</td></tr><tr><td>Authorization</td><td>This is the ZAP Business API Platform authorization token, and must be sent with every API request that requires login.</td></tr></tbody></table>

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

| Key | Value | Description                             |
| --- | ----- | --------------------------------------- |
| Id  | \<id> | The unique ID of the ZAP business user. |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with a 2FA details.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Wed, 19 Feb 2024 23:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
    "success": true,
    "data": {
        "qrCodeUrl": "data:image/png;base64,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",
        "base32Secret": "HI6EWLB6NBYT6RTTO4YGC3SAJA7CY3ZF",
        "message": "2FA Successfully enabled"
    }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name | Type   | Description                                                      |
| ---- | ------ | ---------------------------------------------------------------- |
| 2FA  | Object | Contains information about the ZAP user qrcode url, base secret. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured while processing the request                                                                                                                                                                                                                                                                                     |
