# Create Business Order

### POST /v1/businessOrders <a href="#top" id="top"></a>

Allows a busienss user customer to create an order on the zap pay platform.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to create a business order.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/businessOrders
```

### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
```

#### **Sample request body (crypto - fiat)** <a href="#top" id="top"></a>

<pre class="language-json"><code class="lang-json"><strong>{
</strong>      "amount": 12.52,
      "marketId": "64c13d0ec5efabf7529bfa79",
      "paymentToken": "fda4ue8uvr",
      "customerEmail": "gideon@syxlabs.com" //optional
      "customerId": "64c13d0ec5efabf7529bfa79" // optional and for checkout customers
}
</code></pre>



## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header       | Description      |
| ------------ | ---------------- |
| Content-type | application/json |

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="131">Parameter</th><th width="85">Parm Type</th><th width="99">Data Type</th><th width="101">Required</th><th>Description</th></tr></thead><tbody><tr><td>BusinessOrder</td><td>Body</td><td>BusinessOrder</td><td>Required</td><td>Contains information about business order on ZAP platform. paymentToken, amount, and marketId are required. customerEmail is only used when isApi of payment link data is FALSE and customerId is used when isApi is TRUE.</td></tr></tbody></table>

The properties included in the **Order** object are listed below.

| Property      | Type   | Description                                                                             |
| ------------- | ------ | --------------------------------------------------------------------------------------- |
| paymentToken  | String | The unique token of the payment link.                                                   |
| amount        | Number | The amount the Customer exchanges.                                                      |
| marketId      | String | The unique ID for a specific Market.                                                    |
| customerId    | String | The unique ID for a business customer, gotten from payment link data when isApi is TRUE |
| customerEmail | Object | The email of the customer making a payment.                                             |
| status        | String | The status of the Trade.                                                                |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 201, with information about the new business order.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 201 OK
Date: Wed, 25 Apr 2024 23:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response <a href="#top" id="top"></a>

```json
{
    "success": true,
    "data": {
        "paymentId": {
            "businessId": {
                "email": "gideon@zap.africa",
                "businessName": "erick solutionz",
                "id": "65f1ffb9453cca7421dd08fb"
            },
            "settlementBankDetails": "65f22d0948f667fb5becb3d3",
            "paymentType": "oneTime",
            "id": "65faf10ecc67ff6e0377ff1a"
        },
        "customerId": {
            "name": "gideon",
            "email": "gideon@syxlabs.com",
            "id": "65fb0b445984039244101ef3"
        },
        "amount": 0.52,
        "fees": 14.409449195250374,
        "baseCurrencyToUsdRate": 0.8824993382686411,
        "targetCurrencyToUsdRate": 0.0006369426751592356,
        "targetAmount": 706.0630105672683,
        "marketId": {
            "baseCurrencyId": {
                "name": "Binance-Tether",
                "ticker": "USDTBSC",
                "chainId": "56",
                "isCrypto": true,
                "icon": "https://res.cloudinary.com/dclh3qo14/image/upload/v1688389863/svg/1688389865907.svg",
                "chainIcon": "https://res.cloudinary.com/dukdbbrbc/image/upload/v1684235730/image/bnb.svg",
                "network": "BSC",
                "id": "646369e1e3707ef59b49abe6"
            },
            "targetCurrencyId": {
                "name": "Nigerian Naira",
                "ticker": "NGN",
                "isCrypto": false,
                "icon": "https://res.cloudinary.com/dukdbbrbc/image/upload/v1684234892/image/naira.svg",
                "id": "646369e1e3707ef59b49abef"
            },
            "id": "64c13d0ec5efabf7529bfa79"
        },
        "withdrawalBankAccount": {
            "bankId": {
                "name": "GTBANK PLC",
                "sortCode": "000013",
                "icon": "https://res.cloudinary.com/dukdbbrbc/image/upload/v1683643352/image/1683643352356.png",
                "id": "64afd58f177653c33d9a42a2"
            },
            "accountNumber": "0230974600",
            "accountName": "Stephen Gideon",
            "id": "65f22d0948f667fb5becb3d3"
        },
        "rate": 1385.5239610817666,
        "status": "pending",
        "expiresAt": "2024-03-20T16:43:57.076Z",
        "createdAt": "2024-03-20T16:13:57.084Z",
        "updatedAt": "2024-03-20T16:13:59.014Z",
        "cryptoProviderTxId": "12345566",
        "depositPublicKey": "01234567",
        "id": "65fb0b455984039244101ef8"
    }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name          | Type         | Description                                                 |
| ------------- | ------------ | ----------------------------------------------------------- |
| BusinessOrder | BusiessOrder | Contains information about business orders on ZAP platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |
