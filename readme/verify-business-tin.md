# Verify Business TIN

### POST /v1/verifications/details <a href="#top" id="top"></a>

Allows the Site Admin to verify their business TIN  to the platform.

#### HTTP Method <a href="#top" id="top"></a>

PUT

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to verify a business tin.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/verifications/details
```

#### **Sample request headers** <a href="#top" id="top"></a>

```javascript
'Content-Type: application/json'
```

#### **Sample request body** <a href="#top" id="top"></a>

```json
{
    "businessId": "65c4e6422b8ca01c66b51110",
    "tinNumber": "1239211234910001",
    "isTIN": true
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                             |
| ------------- | ----------------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                                        |
| Authorization | This is the ZAP Business API Platform authorization token, and must be sent with every API request that requires login. |

## Request Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="140">Parameter</th><th width="73">Param Type</th><th width="86">Data Type</th><th width="116">Required</th><th>Description</th></tr></thead><tbody><tr><td>Verification</td><td>Body</td><td>Object</td><td>Required</td><td>Contains information about ZAP platform business tin. businessId, tinNumber and isTin are required.</td></tr></tbody></table>

#### Business Object

Contains information about ZAP's platform business verification.

The properties included in the **Verification** object are listed below. All properties are **required** in the request message.

| Property   | Type    | Description                                  |
| ---------- | ------- | -------------------------------------------- |
| businessId | string  | The unique business user id.                 |
| tinNumber  | string  | The business user tax identification number. |
| isTin      | boolean | identifier that indicates its a tin          |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the logged in business verification.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Wed, 08 Feb 2024 13:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```
{
    "success": true,
    "data": {
        "tinNumber": "1239211234910001",
        "tinVerified": true,
        "createdAt": "2024-02-08T14:26:28.121Z",
        "updatedAt": "2024-02-08T14:26:28.121Z",
        "businessId": "65c4e4945d2869e8324210d8"
    }
}
```

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |
