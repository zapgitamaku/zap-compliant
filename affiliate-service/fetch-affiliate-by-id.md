# Fetch Affiliate By Id

### GET /v1/affiliates/:id <a href="#top" id="top"></a>

Allows a zap affiliate user to fetch their details

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows an affiliate request to fetch their details

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/affiliates/:id
```

#### **Sample request headers** <a href="#top" id="top"></a>

```javascript
'Content-Type: application/json'
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="241">Header</th><th>Description</th></tr></thead><tbody><tr><td>Content-type</td><td>application/json</td></tr><tr><td>Authorization</td><td>This is the ZAP API Platform authorization token, and must be sent with every API request that requires login</td></tr></tbody></table>

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

| Key | Value  | Description                                  |
| --- | ------ | -------------------------------------------- |
| Id  | \<Id>  | The unique ID for the zap affiliate user id. |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with the successful affiliate amounts earned and balance.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Wed, 12 Sep 2023 23:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
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
    },
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

