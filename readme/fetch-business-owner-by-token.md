# Fetch Business Owner By Token

### GET /v1/business/token/:token <a href="#top" id="top"></a>

Allows the Site Admin to get a business owner on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to fetch a specified business owner.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/business/token/:token
```

### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

#### For Invited Owners: <a href="#top" id="top"></a>

```
'owner-auth: 63e0f4da81979dcc3b9ee123-1c927684-066d-4c2c-b5c5-a4995f040618'
```

## Request Parameter <a href="#samplerequest" id="samplerequest"></a>

| Paramater | Description                                                                                                                       |
| --------- | --------------------------------------------------------------------------------------------------------------------------------- |
| token     | If its an invited owner, the owner token can be gotten from the splitting of the owner auth ( the 2nd  value in the split array). |

## Request Header <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="204">Header</th><th>Description</th></tr></thead><tbody><tr><td>Content-type</td><td>application/json</td></tr><tr><td>Authorization</td><td>This is the ZAP Business API Platform authorization token, and must be sent with every API request that requires login.</td></tr><tr><td>owner-auth</td><td>This is the token sent along the invitation link and should be used when invited owner are interacting with platform.</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with a owner.

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
        "businessId": "65c4e4945d2869e8324210d8",
        "email": "johndoe@gmail.com",
        "phoneNumber": "2347030839847",
        "bvn": {
            "bvnVerified": true
        },
        "createdAt": "2024-02-08T14:26:28.121Z",
        "updatedAt": "2024-02-08T14:26:28.121Z",
        "id": "65c4e445d2869k342421927"
    }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name  | Type   | Description                                                  |
| ----- | ------ | ------------------------------------------------------------ |
| owner | Object | Contains information about the ZAP platform business  owner. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured while processing the request                                                                                                                                                                                                                                                                                     |
