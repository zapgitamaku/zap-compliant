# Forgot Password

### POST /v1/business/forgotPassword <a href="#top" id="top"></a>



Allows the Zap business user to receive an email to initiate password reset..

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to initiate password reset.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/business/forgotPassword
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
    "email":"johndoe@example.com"
}
```

## Request Body <a href="#samplerequest" id="samplerequest"></a>

| Parameter | Parameter Type | Data Type | Required | Description                                                                                     |
| --------- | -------------- | --------- | -------- | ----------------------------------------------------------------------------------------------- |
| Business  | Body           | Object    | Required | Contains information about ZAP platform business owner. Business User unique email is required. |

### Business Object <a href="#samplerequest" id="samplerequest"></a>

Contains information about ZAP's platform business

The properties included in the **Business** object are listed below. All properties are **required** in the request message.

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with a 2FA details.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

| Property | Type   | Description                                                                                         |
| -------- | ------ | --------------------------------------------------------------------------------------------------- |
| email    | String | <p>The business user unique email address.</p><p>Max length: 320 chars. Standard email pattern.</p> |

### Sample Response

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
        "token": "token data",
        "message": "Please check your email to continue password reset"
    }
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
| 500  | An error occured while processing the request                                                                                                                                                                                                                                                                                     |
