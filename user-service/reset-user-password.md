# Reset User Password

### POST /v1/forgotPassword <a href="#top" id="top"></a>

Allows the Site Admin to reset the password of a user on the platform.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to reset a specified user's password.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/forgotPassword/
```

#### **Sample request headers** <a href="#top" id="top"></a>

```javascript
'Content-Type: application/json'
```

#### **Sample** Request Body <a href="#top" id="top"></a>

<pre class="language-json"><code class="lang-json">{
<strong>        "identity": "adminagent@zap.com",
</strong>        "otp": "fee325666ab",
        "newPassword": "n3wP@ssw0rd",
}
</code></pre>

## Request Header <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="241">Header</th><th>Description</th></tr></thead><tbody><tr><td>Content-type</td><td>application/json</td></tr><tr><td>Authorization</td><td>This is the ZAP API Platform authorization token, and must be sent with every API request that requires login</td></tr></tbody></table>

#### UserData Object

Contains updated information about the particular ZAP platform user.

This array is returned by the following operations:

* #### POST /api/v1/forgotPassword

## Request Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="108">Parameter</th><th width="162">Param Type</th><th>Data Type</th><th>Required</th><th>Description</th></tr></thead><tbody><tr><td>User</td><td>Body</td><td>Object</td><td>Required</td><td>Contains information about ZAP platform user. userId, email, secureOTP and new Password are required.</td></tr></tbody></table>

#### User Object

Contains information about ZAP's platform user.

This object is used by the following operations:

* #### POST /api/v1/forgotPassword

The properties included in the **User** object are listed below. All properties are **optional** in the request message.

| Property    | Type   | Description                                                                                      |
| ----------- | ------ | ------------------------------------------------------------------------------------------------ |
| identity    | string | <p>The user's email address or username</p><p>Standard email pattern or Zap username pattern</p> |
| otp         | string | The secure OTP                                                                                   |
| newPassword | string | The new secure password                                                                          |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with a success message.

And the Password reset OTP is sent to the user's email address

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
    "data": "Password reset link sent to user's email address"
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name    | Type   | Description                                         |
| ------- | ------ | --------------------------------------------------- |
| message | string | Contains confirmation about reset password request. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured while processing the request                                                                                                                                                                                                                                                                                     |

