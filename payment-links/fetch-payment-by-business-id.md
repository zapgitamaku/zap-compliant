# Fetch Payment by Business Id

### GET /v1/payment/business/:businessId <a href="#top" id="top"></a>

Allows the Site Admin to get an available payment on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to fetch a list of payment.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/payment/business/:businessId
```

### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

## Request Parameter <a href="#samplerequest" id="samplerequest"></a>

| Paramater | Description                         |
| --------- | ----------------------------------- |
| id        | The unique id of the business user. |

## Request Header <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="182">Header</th><th>Description</th></tr></thead><tbody><tr><td>Content-type</td><td>application/json</td></tr><tr><td>Authorization</td><td>This is the ZAP Business API Platform authorization token, and must be sent with every API request that requires login.</td></tr></tbody></table>

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
            "settlementBankDetails": {
                "bankId": "64afd58f177653c33d9a4220",
                "businessId": "65eef259501d4e3cbc2cff1d",
                "accountNumber": "1234567890",
                "accountName": "JOHN DOE DON",
                "primaryAccount": false,
                "createdAt": "2024-03-11T12:16:20.698Z",
                "updatedAt": "2024-03-11T14:56:37.371Z",
                "id": "65eef614cf9c648ad9b69ba0"
            },
            "description": "test payment",
            "paymentType": "oneTime",
            "paymentLink": "https://pay.business.zap.africa/6X5Qcwl357",
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
        },
        {
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
            "settlementBankDetails": {
                "bankId": "64afd58f177653c33d9a4220",
                "businessId": "65eef259501d4e3cbc2cff1d",
                "accountNumber": "1234567890",
                "accountName": "JOHN DOE DON",
                "primaryAccount": false,
                "createdAt": "2024-03-11T12:16:20.698Z",
                "updatedAt": "2024-03-11T14:56:37.371Z",
                "id": "65eef614cf9c648ad9b69ba0"
            },
            "description": "test payment",
            "paymentType": "oneTime",
            "paymentLink": "https://pay.business.zap.africa/yB45rx9nCB",
            "paymentToken": "yb45rx9ncb",
            "customerId": [],
            "amount": 0,
            "deliverReceipt": true,
            "isApi": false,
            "status": "active",
            "isDeleted": false,
            "createdAt": "2024-03-11T12:25:55.435Z",
            "updatedAt": "2024-03-11T12:25:55.435Z",
            "id": "65eef853cf264b964634dc81"
        },
        {
            "businessId": "65eef259501d4e3cbc2cff1d",
            "productId": [
                {
                    "businessId": "65eef259501d4e3cbc2cff1d",
                    "name": "Johnie Body Cream",
                    "description": "Johnie Body Cream for men",
                    "image": "https://res.cloudinary.com/name/image/upload/v1710237721/business-product-development/2c0421d4-aaad-4050-aa1a-d0012c6b3495.jpg",
                    "price": 309,
                    "createdAt": "2024-03-12T10:02:02.618Z",
                    "updatedAt": "2024-03-12T10:02:02.618Z",
                    "id": "65f0281ab34eff81de0cd16c"
                }
            ],
            "settlementBankDetails": {
                "bankId": "64afd58f177653c33d9a4228",
                "businessId": "65eef259501d4e3cbc2cff1d",
                "accountNumber": "1234567899",
                "accountName": "JOHN DOE DON",
                "primaryAccount": true,
                "createdAt": "2024-03-11T13:40:56.889Z",
                "updatedAt": "2024-03-12T09:43:06.971Z",
                "id": "65ef09e8e3c4c66cdc380afd"
            },
            "description": "test payment",
            "paymentType": "oneTime",
            "paymentLink": "https://pay.business.zap.africa/eapq1k36ku",
            "paymentToken": "eapq1k36ku",
            "customerId": [],
            "amount": 927,
            "deliverReceipt": true,
            "isApi": false,
            "status": "active",
            "isDeleted": false,
            "createdAt": "2024-03-12T10:09:49.339Z",
            "updatedAt": "2024-03-12T10:09:49.339Z",
            "id": "65f029ed76a7659c692808f8"
        }
    ]
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name    | Type  | Description                                       |
| ------- | ----- | ------------------------------------------------- |
| payment | Array | Contains array of information about bank details. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured while processing the request                                                                                                                                                                                                                                                                                     |
