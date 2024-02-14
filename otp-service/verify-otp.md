# Verify OTP

### POST /v1/otp/verify <a href="#top" id="top"></a>

Allows the Site Admin to verify a user's secure OTP during an operation on the platform.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to verify an OTP for a user.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/otp/verify
```

#### **Sample request headers** <a href="#top" id="top"></a>

```javascript
'Content-Type: application/json'
```

#### &#x20;**Sample request body** <a href="#top" id="top"></a>

> Identity can be either email or phoneNumber

```json
// Verify using email
{
    "otp": "573587",
    "identity": "adminuser@zap.com"
}

// Verify using phoneNumber
{
    "otp": "573587",
    "identity": "+2348011111111"
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header       | Description      |
| ------------ | ---------------- |
| Content-type | application/json |

## Request Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="108">Parameter</th><th width="162">Param Type</th><th>Data Type</th><th>Required</th><th>Description</th></tr></thead><tbody><tr><td>User</td><td>Body</td><td>Object</td><td>Required</td><td>Contains information about ZAP platform user. Email/PhoneNumber and Secure OTP are required.</td></tr></tbody></table>

#### User Object

Contains information about ZAP's platform user.

This object is used by the following operations:

* #### POST /api/v1/otp/

The properties included in the **User** object are listed below. All properties are **required** in the request message.

| Property | Type   | Description                                                                                        |
| -------- | ------ | -------------------------------------------------------------------------------------------------- |
| identity | string | <p>The user's email address, or username</p><p>Standard email pattern. or Zap Username Pattern</p> |
| otp      | string | The Secure OTP sent to the user's email                                                            |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with success verification message.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Wed, 25 Jan 2023 23:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```
{
    "success": true,
    "data": "OTP verified"
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name | Type   | Description                                                 |
| ---- | ------ | ----------------------------------------------------------- |
| Data | String | Contains success information about the Secure OTP verified. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |

