# Fetch Products

### GET /v1/product/business/:businessId <a href="#top" id="top"></a>

Allows the Site Admin to get business products on the platform or zap pay.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to fetch specified business user products.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/product/business/:businessId
```

### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

#### For invited owner: <a href="#top" id="top"></a>

```
'Content-Type: application/json'
api-key: wjjmaesvms37w30sdoneox2l3homvbytlhf320s2
```

## Request Parameter <a href="#samplerequest" id="samplerequest"></a>

| Paramater  | Description                      |
| ---------- | -------------------------------- |
| businessId | The unique of the business user. |

## Request Header <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="182">Header</th><th>Description</th></tr></thead><tbody><tr><td>Content-type</td><td>application/json</td></tr><tr><td>Authorization</td><td>This is the ZAP Business API Platform authorization token, and must be sent with every API request that requires login.</td></tr><tr><td>api-key</td><td>This is the api key for the zap pay communication with the platform.</td></tr></tbody></table>

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
        "businessId": "65e71840973f0e97fb99849d",
        "name": "test Product",
        "description": "testing product",
        "image": "https://res.cloudinary.com/dukdbbrbc/image/upload/v1709659340/business-verification-production/45e61817-b8c4-446c-8513-b74728a79bf9.png",
        "price": 1000,
        "createdAt": "2024-03-05T17:22:22.175Z",
        "updatedAt": "2024-03-05T17:22:22.175Z",
        "id": "65e754ce2b2a2d15c1dadca7"
     }
  ]
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name    | Type   | Description                                            |
| ------- | ------ | ------------------------------------------------------ |
| product | Object | Contains information about the ZAP business  products. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured while processing the request                                                                                                                                                                                                                                                                                     |
