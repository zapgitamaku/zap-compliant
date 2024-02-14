# Fetch Verifications

### GET /v1/verifications <a href="#top" id="top"></a>

Allows a User to fetch all verification data on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to get all verification data.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/verifications
```

#### &#x20;**Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                              |
| Authorization | This is the ZAP API Platform authorization token, and must be sent with every API request that requires login |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the new bank.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Wed, 01 Mar 2023 00:48:10 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

````json
{
    "success": true,
    "data": {
        "verificationData": [
{
                "userId": "6410e2b1bc3d3821133a90f9",
                "documentId": "12345asdfgh112",
                "documentType": "residence",
                "documentUrl": "https://res.cloudinary.com/dwwttestc/image/upload/v16793435355/user-verification/09-3.jpg",
                "status": "pending",
                "comments": "",
                "createdAt": "2023-03-17T10:11:43.565Z",
                "updatedAt": "2023-03-22T03:05:09.603Z",
                "id": "64143cdf122356ace4dd6"
            },
```
        ],
        "bodyLimit": 10,
        "pageLimit": 1,
        "dataCount": 1
    }
}
````

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name         | Type         | Description                                                     |
| ------------ | ------------ | --------------------------------------------------------------- |
| Verification | Verification | Contains information about  Verification data on ZAP  platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                   |
| ---- | --------------------------------------- |
| 404  | The resource could not be found.        |
| 500  | An error occured processing the request |

