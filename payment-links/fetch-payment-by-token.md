# Fetch Payment by Token

### GET /v1/payment/token/:token <a href="#top" id="top"></a>

Allows the Site Admin to get an available payment on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to fetch a paymenk details.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/payment/token/:token
```

### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
```

## Request Parameter <a href="#samplerequest" id="samplerequest"></a>

| Paramater | Description                      |
| --------- | -------------------------------- |
| token     | The unique token of the payment. |

## Request Header <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="182">Header</th><th>Description</th></tr></thead><tbody><tr><td>Content-type</td><td>application/json</td></tr></tbody></table>

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
        "businessId": "65eef259501d4e3cbc2cff1d",
        "productId": [
            {
                "businessId": "65eedd391b4fe4aa7d156472",
                "name": "Johnie Face Cream",
                "description": "Johnie Face Cream for men",
                "image": "https://res.cloudinary.com/name/image/upload/v1710154636/business-product-development/ed8bf289-807e-465e-9942-d66e637fe8d1.jpg",
                "price": 300,
                "createdAt": "2024-03-11T10:57:17.037Z",
                "updatedAt": "2024-03-11T10:57:17.037Z",
                "id": "65eee38d84dd365ab0635126"
            }
        ],
        "settlementBankDetails": "65eef614cf9c648ad9b69ba0",
        "description": "test payment",
        "paymentType": "oneTime",
        "paymentLink": "undefined/6X5Qcwl357",
        "paymentToken": "6x5qcwl357",
        "customerId": [],
        "amount": 0,
        "deliverReceipt": true,
        "isApi": false,
        "status": "active",
        "isDeleted": false,
        "createdAt": "2024-03-11T12:24:07.710Z",
        "updatedAt": "2024-03-11T12:24:07.710Z",
        "id": "65eef7e7cf9c648ad9b69bab"
    }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name    | Type   | Description                           |
| ------- | ------ | ------------------------------------- |
| payment | Object | Contains information about a payment. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured while processing the request                                                                                                                                                                                                                                                                                     |
