# Fetch Users Details from Jwt

### GET /v1/users/token <a href="#top" id="top"></a>

Allows the user  to get their details from the jwt on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to fetch a user details from jwt.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/users/token
```

#### **Sample request headers** <a href="#top" id="top"></a>

```javascript
'Content-Type: application/json'
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="241">Header</th><th>Description</th></tr></thead><tbody><tr><td>Content-type</td><td>application/json</td></tr><tr><td>Authorization</td><td>This is the ZAP API Platform authorization token, and must be sent with every API request that requires login</td></tr></tbody></table>

#### UserData Object

Contains information about the specified ZAP platform user.

This array is returned by the following operations:

* #### GET /api/v1/users

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with a user.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Wed, 25 Jan 2023 23:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

````json
```json
{
    "success": true,
    "data": {
        "userVerification": {
            "idVerification": {
                "status": "pending",
                "verificationLevel": 1,
                "id": "648c769461535465ef26128b"
            }
        },
        "bvn": {
            "bvnVerified": false
        },
        "twoFA": {
            "secret": "",
            "enabled": false
        },
        "receiveEmailNotifications": true,
        "name": "John Knight",
        "email": "johnknight@gmail.com",
        "roleId": {
            "name": "user",
            "permissions": [
                "banks:readAny",
                "bankDetails:read",
                "bankDetails:write",
                "currencies:readAny",
                "markets:readAny",
                "orders:read",
                "orders:write",
                "users:read",
                "users:write",
                "monitor:read",
                "trades:read",
                "verifications:read",
                "verifications:write",
                "faqs:readAny",
                "faqs:writeAny",
                "roles:read",
                "supportConversations:write",
                "supportConversations:read"
            ],
            "id": "6438a0da6b23108861009e51"
        },
        "emailVerified": true,
        "userAgent": [
            "Mozilla/5.0 (X11; Linux aarch64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/88.0.4324.188 Safari/537.36 CrKey/1.54.250320",
            "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/605.1.15 (KHTML, like Gecko) Version/16.5 Safari/605.1.15",
            "PostmanRuntime/7.32.2",
            "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/112.0.0.0 Safari/537.36",
            "PostmanRuntime/7.32.3"
        ],
        "createdAt": "2023-06-05T13:59:02.464Z",
        "updatedAt": "2023-06-20T13:24:21.457Z",
        "id": "647dea2605647ed1d5193n7a"
    }
}
```
````

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name     | Type   | Description                                       |
| -------- | ------ | ------------------------------------------------- |
| userData | Object | Contains information about the ZAP platform user. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured while processing the request                                                                                                                                                                                                                                                                                     |

