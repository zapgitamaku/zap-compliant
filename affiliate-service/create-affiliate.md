# Create Affiliate

### POST /v1/affiliates <a href="#top" id="top"></a>

Allows a zap user to become an affiliate on the platform.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to become an affiliate.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/affiliates
```

#### **Sample request headers** <a href="#top" id="top"></a>

```javascript
'Content-Type: application/json'
```

#### **Sample request body** <a href="#top" id="top"></a>

```json
{
    "userId": 12345678909876543211235813,
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header       | Description      |
| ------------ | ---------------- |
| Content-type | application/json |

## Request Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="108">Parameter</th><th width="113">Param Type</th><th width="100">Data Type</th><th width="101">Required</th><th>Description</th></tr></thead><tbody><tr><td>User</td><td>Body</td><td>Object</td><td>Required</td><td>Contains information about ZAP platform user. userId is required.</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 201, with information about the affiliate user.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 201 OK
Date: Wed, 12 Sep 2023 23:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```
{
    "success": true,
    "data": {
        "userId": 12345678909876543211235813,
        "affiliateAmountEarned": 0,
        "affiliateAmountWithdrawn": 0,
        "affiliateTransactionCount": 0,
        "affiliateQuota": 0,
        "referredCompleteUsers": 0,
        "createdAt": "2023-09-12T11:54:50.489Z",
        "updatedAt": "2023-09-12T11:54:50.489Z",
        "id": "63fc9a0a29dc8cbccf38d096"
    }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name | Type | Description                                                      |
| ---- | ---- | ---------------------------------------------------------------- |
| User | User | Contains information about ZAP's platform user affiliate detais. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |

