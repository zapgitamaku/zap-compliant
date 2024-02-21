# Fetch Business User By Id

### GET /v1/business/:id <a href="#top" id="top"></a>

Allows the Site Admin to get a business user on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to fetch a specified business user.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/business/:id
```

#### **Sample request headers** <a href="#top" id="top"></a>

```javascript
'Content-Type: application/json'
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="241">Header</th><th>Description</th></tr></thead><tbody><tr><td>Content-type</td><td>application/json</td></tr><tr><td>Authorization</td><td>This is the ZAP Business API Platform authorization token, and must be sent with every API request that requires login.</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with a business.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Wed, 09 Feb 2024 23:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
    "success": true,
    "data": {
        "firstName": "john",
        "lastName": "doe",
        "email": "johndoe@gmail.com",
        "phoneNumber": "2347030839847",
        "phoneNumberVerified": false,
        "password": "$2b$10$5zrcihvQ0yJA.i25cvShAOe9qLgh3RwugP.nln/hZPrl/CD281a8O",
        "bvn": {
            "bvnVerified": false
        },
        "businessName": "Space stocks",
        "numberOfBusinessOwner": 0,
        "numberOfBusinessOwnerFullyVerified": 0,
        "iPAddress": [],
        "emailVerified": false,
        "twoFA": {
            "enabled": false
        },
        "userAgent": [],
        "receiveEmailNotifications": true,
        "transactionVolume": 0,
        "createdAt": "2024-02-08T14:26:28.121Z",
        "updatedAt": "2024-02-08T14:26:28.121Z",
        "id": "65c4e4945d2869e8324210d8"
    }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name     | Type   | Description                                           |
| -------- | ------ | ----------------------------------------------------- |
| business | Object | Contains information about the ZAP platform business. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured while processing the request                                                                                                                                                                                                                                                                                     |
