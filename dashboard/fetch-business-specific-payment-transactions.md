# Fetch Business Specific Payment Transactions

### GET /v1/order/link/:paymentId <a href="#top" id="top"></a>

Allows the Site Admin to get the business user specific payment link successful transactions on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to fetch a business user payment link successful transaction.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/order/link/:paymentId
```

### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

## Request Parameter <a href="#samplerequest" id="samplerequest"></a>

| Paramater | Description                        |
| --------- | ---------------------------------- |
| paymentId | The unique id of the payment link. |

## Request Header <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="182">Header</th><th>Description</th></tr></thead><tbody><tr><td>Content-type</td><td>application/json</td></tr><tr><td>Authorization</td><td>This is the ZAP Business API Platform authorization token, and must be sent with every API request that requires login.</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with stats.

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
            "paymentId": {
                "businessId": "6602a6b02837aa07ee58dcc2",
                "products": [
                    {
                        "productId": "6603ed67cc80579cc5e9cb80",
                        "quantity": 1
                    }
                ],
                "settlementBankDetails": "6604032d701799b6ddf8c0ab",
                "title": "Payment Link 1",
                "description": "Payment Link 1",
                "paymentType": "oneTime",
                "paymentLink": "https://dev.pay.zap.africa/fda4ue8uVR",
                "paymentToken": "fda4ue8uvr",
                "customerId": [],
                "amount": 50000,
                "deliverReceipt": true,
                "isApi": true,
                "status": "active",
                "isDeleted": false,
                "createdAt": "2024-03-27T13:43:52.737Z",
                "updatedAt": "2024-03-27T13:43:52.737Z",
                "keyId": "66015ff2c42d2fbd9be8a2ec",
                "id": "66042298f5d9138d874bcfb8"
            },
            "customerId": "66056fb5602bfd2cb7b7db3f",
            "amount": 12.52,
            "fees": 287.38986558333005,
            "baseCurrencyToUsdRate": 0.9182334968051118,
            "targetCurrencyToUsdRate": 0.0008,
            "targetAmount": 14082.964359416668,
            "marketId": "64c13d0ec5efabf7529bfa79",
            "withdrawalBankAccount": "6604032d701799b6ddf8c0ab",
            "rate": 1147.7918710063898,
            "status": "filled",
            "expiresAt": "2024-03-28T13:55:13.123Z",
            "createdAt": "2024-03-28T13:25:13.129Z",
            "updatedAt": "2024-03-28T13:25:16.125Z",
            "cryptoProviderTxId": "fe0de58166307b",
            "depositPublicKey": "0xd178214fA9368A15318fF6bc751083F286c1e375",
            "confirmedAt": "2024-03-28T13:25:16.125Z",
            "id": "66056fb9602bfd2cb7b7db4f"
        }
    ]
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name    | Type   | Description                                                  |
| ------- | ------ | ------------------------------------------------------------ |
| Payment | Object | Contains the business user payment link transaction history. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured while processing the request                                                                                                                                                                                                                                                                                     |
