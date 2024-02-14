# LogOut User By Id

### PUT /v1/users/logout/:id <a href="#top" id="top"></a>

Allows the user to logout on the platform.

#### HTTP Method <a href="#top" id="top"></a>

PUT

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to modify a specified user.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/users/logout/:id
```

#### **Sample request headers** <a href="#top" id="top"></a>

```javascript
'Content-Type: application/json'
```

#### **Sample** Request Body <a href="#top" id="top"></a>

```json
{
 "deviceToken": "fgYo5k5yrt9KaswddR4s5:APA91bFqeRBWioAOysyHLdLn5D--R36Izk5cXF0E-5nIdai-IrOw1bWv-O0BV6RQMLXJyAU8Gh27g6u573B1mI01-HEla5_Xat-r02nPKxJHEXwZtbZDzlf4o_fCR7XdN0ZHNuIZswaiLMK"
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="241">Header</th><th>Description</th></tr></thead><tbody><tr><td>Content-type</td><td>application/json</td></tr><tr><td>Authorization</td><td>This is the ZAP API Platform authorization token, and must be sent with every API request that requires login</td></tr></tbody></table>

## Request Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="95">Parameter</th><th width="92">Param Type</th><th width="105">Data Type</th><th width="118">Required</th><th>Description</th></tr></thead><tbody><tr><td>User</td><td>Body</td><td>Object</td><td>Required</td><td>Contains information about ZAP platform user device token. deviceToken is required.</td></tr></tbody></table>

#### User Object

The properties included in the **User** object are listed below.&#x20;

| Property     | Type   | Description                  |
| ------------ | ------ | ---------------------------- |
| deviceToken  | string | the device token of the user |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with an updated user details.

If the request body contains email, the operation returns a HTTP status code 200.

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
    "data": "Logout Successfull"
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

