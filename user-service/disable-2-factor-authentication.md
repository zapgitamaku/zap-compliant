# Disable 2 Factor Authentication

### POST /v1/users/:id/disable2fa <a href="#top" id="top"></a>

Allows the zap user to enable 2FA on the platform.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to enable 2FA.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/users/:id/disable2fa
```

#### **Sample request headers** <a href="#top" id="top"></a>

```javascript
'Content-Type: application/json'
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="241">Header</th><th>Description</th></tr></thead><tbody><tr><td>Content-type</td><td>application/json</td></tr><tr><td>Authorization</td><td>This is the ZAP API Platform authorization token, and must be sent with every API request that requires login</td></tr></tbody></table>

#### &#x20;**Sample request body** <a href="#top" id="top"></a>

```json
{
    "password": "MyS3cureP@ssw0r4"
}
```

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

| Key | Value | Description                    |
| --- | ----- | ------------------------------ |
| Id  | \<id> | The unique id of the Zap User. |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with a 2FA details.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Wed, 19 Jun 2023 23:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
    "success": true,
    "data": "2FA disabled Successfully"
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name     | Type   | Description                   |
| -------- | ------ | ----------------------------- |
| response | Object | Contains the success message. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured while processing the request                                                                                                                                                                                                                                                                                     |

