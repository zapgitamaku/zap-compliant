# Verify OTP Login

### POST /v1/login/verify-otp <a href="#top" id="top"></a>

Allows the Site Admin to verify a new or existing user's otp and log the user into the platform.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to create a user.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/login/verify-otp
```

#### **Sample request headers** <a href="#top" id="top"></a>

```javascript
'Content-Type: application/json'
```

#### **Sample request body** <a href="#top" id="top"></a>

```json
{
    "email": "myemailaddress@myemail.com",
    "otp": "123456",
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header       | Description      |
| ------------ | ---------------- |
| Content-type | application/json |

## Request Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="108">Parameter</th><th width="162">Param Type</th><th>Data Type</th><th>Required</th><th>Description</th></tr></thead><tbody><tr><td>User</td><td>Body</td><td>Object</td><td>Required</td><td>Contains information about ZAP platform user. Email and otp are required.</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 201 for a new user and 200 for an existing user with information about the new user.

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
    "data": {
        "bvn": {
            "bvnVerified": false
        },
        "twoFA": {
            "enabled": false
        },
        "username": null,
        "email": "myemailaddress@myemail.com",
        "phoneNumberVerified": false,
        "roleId": "6438a0da6b23108861009e51",
        "iPAddress": [
            "::1"
        ],
        "emailVerified": true,
        "firstTransaction": false,
        "viewedTooltipOnMobile": false,
        "viewedTooltipOnWeb": false,
        "userAgent": [
            "PostmanRuntime/7.42.0"
        ],
        "receiveEmailNotifications": true,
        "isAffiliate": false,
        "transactionVolume": 0,
        "referralAmountEarned": 0,
        "referralAmountWithdrawn": 0,
        "restrictedTransactionVolume": 0,
        "fullyVerifiedAt": null,
        "fullyVerified": false,
        "restrictedTransactionTotal": 0,
        "failedLoginAttempt": 0,
        "deviceToken": [],
        "freeZapCount": 0,
        "flags": [],
        "createdAt": "2024-11-26T10:26:21.013Z",
        "updatedAt": "2024-11-26T10:49:00.669Z",
        "preferenceId": "6745a36cc7b6cc130ff6cdca",
        "id": "6745a24d117bbe3b7b13d066",
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyIjp7ImVtYWlsIjoiYW1ha3VAemFwLmFmcmljYSIsInJvbGVJZCI6IjY0MzhhMGRhNmIyMzEwODg2MTAwOWU1MSIsImlkIjoiNjc0NWEyNGQxMTdiYmUzYjdiMTNkMDY2In0sImlhdCI6MTczMjYxODE0MCwiZXhwIjoxNzMyNjM5NzQwfQ.70jmSydVJU9LXQZo7qWXmX8QfFLPIlz7YG3x5myDTQk",
        "refreshToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyIjp7ImVtYWlsIjoiYW1ha3VAemFwLmFmcmljYSIsInJvbGVJZCI6IjY0MzhhMGRhNmIyMzEwODg2MTAwOWU1MSIsImlkIjoiNjc0NWEyNGQxMTdiYmUzYjdiMTNkMDY2In0sImlhdCI6MTczMjYxODE0MCwiZXhwIjoxNzQwMzk0MTQwfQ.5AR4JpSezd6YSy5NdGanSp5YIKTg9uGyKiYjJdArJQg"
    }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name | Type | Description                                     |
| ---- | ---- | ----------------------------------------------- |
| User | User | Contains information about ZAP's platform user. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |
