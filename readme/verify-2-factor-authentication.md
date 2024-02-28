# Verify 2 Factor Authentication

### POST /v1/business/verify2fa/:id <a href="#top" id="top"></a>

Allows the zap business user to verify 2FA on the platform..

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to verify 2FA.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/business/verify2fa/:id
```

#### **Sample request headers** <a href="#top" id="top"></a>

```javascript
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="241">Header</th><th>Description</th></tr></thead><tbody><tr><td>Content-type</td><td>application/json</td></tr><tr><td>Authorization</td><td>This is the ZAP Business API Platform authorization token, and must be sent with every API request that requires login.</td></tr></tbody></table>

#### **Sample request body** <a href="#top" id="top"></a>

```json
{
    "token": "890478"
}
```

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
    "data": "Token verified successfully"
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name | Type   | Description                  |
| ---- | ------ | ---------------------------- |
| 2FA  | Object | Contains the success message |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured while processing the request                                                                                                                                                                                                                                                                                     |
