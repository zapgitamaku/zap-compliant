# Fetch Payment by Id

### GET /v1/payment/:id <a href="#top" id="top"></a>

Allows the Site Admin to get an available payment on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to fetch a specific payment.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/payment/:id
```

### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

## Request Parameter <a href="#samplerequest" id="samplerequest"></a>

| Paramater | Description                            |
| --------- | -------------------------------------- |
| id        | The unique id of the business payment. |

## Request Header <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="182">Header</th><th>Description</th></tr></thead><tbody><tr><td>Content-type</td><td>application/json</td></tr><tr><td>Authorization</td><td>This is the ZAP Business API Platform authorization token, and must be sent with every API request that requires login.</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with a payment detail.

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
        "businessId": "65fd7554938c4c2dbf6df623",
        "products": [
            {
                "productId": {
                    "businessId": "65fd7554938c4c2dbf6df623",
                    "name": "Dexie Detective",
                    "description": "We solve crimes",
                    "image": "https://s3.eu-north-1.amazonaws.com/zap.africa/other-documents/1711109557799edo2_1686644109.jpg",
                    "price": 100000,
                    "revenue": 0,
                    "unitSold": 0,
                    "isDeleted": false,
                    "createdAt": "2024-03-22T12:12:38.616Z",
                    "updatedAt": "2024-03-22T12:12:38.616Z",
                    "id": "65fd75b6938c4c2dbf6df65a"
                },
                "quantity": 1
            }
        ],
        "settlementBankDetails": "65fd76e5938c4c2dbf6df6f2",
        "description": "we are testing",
        "paymentType": "oneTime",
        "paymentLink": "https://pay.zap.africa/gw4VPCBbH6",
        "paymentToken": "gw4vpcbbh6",
        "customerId": [],
        "amount": 100000,
        "deliverReceipt": false,
        "isApi": false,
        "status": "active",
        "isDeleted": false,
        "createdAt": "2024-03-22T12:18:57.976Z",
        "updatedAt": "2024-03-22T12:18:57.976Z",
        "id": "65fd7731938c4c2dbf6df71c"
    }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name    | Type   | Description                                       |
| ------- | ------ | ------------------------------------------------- |
| payment | Object | Contains array of information about payment link. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured while processing the request                                                                                                                                                                                                                                                                                     |
