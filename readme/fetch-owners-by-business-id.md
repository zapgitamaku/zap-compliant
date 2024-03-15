# Fetch Owners By Business Id

### GET /v1/owner/business/:businessId <a href="#top" id="top"></a>

Allows the Zap Business User to get all their owners

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to fetch business owners.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/owner/business/:businessId
```

### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

## Request Parameter <a href="#samplerequest" id="samplerequest"></a>

| Paramater  | Description                 |
| ---------- | --------------------------- |
| businessId | The business user unique id |

## Request Header <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="204">Header</th><th>Description</th></tr></thead><tbody><tr><td>Content-type</td><td>application/json</td></tr><tr><td>Authorization</td><td>This is the ZAP Business API Platform authorization token, and must be sent with every API request that requires login.</td></tr></tbody></table>

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
    "data": [
        {
            "bvn": {
                "bvnName": "JOHN DOE",
                "bvnVerified": true
            },
            "businessId": {
                "firstName": "PRECIOUS",
                "lastName": "VINCENT",
                "id": "65e87c673af30b7d163fd940"
            },
            "firstName": "John",
            "lastName": "Doe",
            "email": "john@gmail.com",
            "phoneNumber": "07030839847",
            "dob": "20-05-2000",
            "gender": "male",
            "nationality": "nigerian",
            "role": "shareholder",
            "status": "approved",
            "createdAt": "2024-02-12T11:21:31.523Z",
            "updatedAt": "2024-02-12T12:39:27.842Z",
            "documentId": "96816564951",
            "documentIdType": "nin",
            "id": "65c9ff3b531881155581f74a"
        }
    ]
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name  | Type   | Description                                                   |
| ----- | ------ | ------------------------------------------------------------- |
| owner | Object | Contains information about the ZAP platform business  owners. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured while processing the request                                                                                                                                                                                                                                                                                     |
