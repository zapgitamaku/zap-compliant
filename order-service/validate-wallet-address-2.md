---
description: Endpoint to get details and balance of a wallet.
---

# Get Balance of tokens

### GET /v1/orders/balance/tokens <a href="#top" id="top"></a>

Gets details of an account and its balances based on the chainId

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to validate a zap user receiving wallet address on the platform.

#### **Sample request** URL <a href="#top" id="top"></a>

<pre><code><strong>v1/orders/balance/tokens
</strong></code></pre>

#### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header       | Description      |
| ------------ | ---------------- |
| Content-type | application/json |

## Request Query <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="125">Key</th><th>Value</th><th>Description</th></tr></thead><tbody><tr><td>chainId</td><td>String</td><td>The chainId of the address</td></tr><tr><td>walletAddress</td><td>String</td><td>The wallet address to be checked.</td></tr></tbody></table>

#### **Sample request body** <a href="#top" id="top"></a>

```json
{
    "chainId": "56"
    "walletAddress": "0x5a52e96bacdabb82fd05763e25335261b270efcb",
}
```

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the updated order.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Wed, 27 Jul 2023 15:54:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
    "success": true,
    "data": [
        {
            "name": "Binance USDC",
            "ticker": "USDCBSC",
            "chainId": "56",
            "icon": "https://res.cloudinary.com/dukdbbrbc/image/upload/v1699375981/icons/1699375981004.svg",
            "price": "1.0024797019503837",
            "percentageChange1hr": "0.00",
            "percentageChange24hr": "-0.31",
            "balance": "0.0"
        },
        {
            "name": "Binance-Coin",
            "ticker": "BNBBSC",
            "chainId": "56",
            "icon": "https://res.cloudinary.com/dukdbbrbc/image/upload/v1684235730/image/bnb.svg",
            "price": "531.2156208727401",
            "percentageChange1hr": "0.73",
            "percentageChange24hr": "-2.94",
            "balance": "0.069298278771210129"
        },
        {
            "name": "Binance-Tether",
            "ticker": "USDTBSC",
            "chainId": "56",
            "icon": "https://res.cloudinary.com/dclh3qo14/image/upload/v1688389863/svg/1688389865907.svg",
            "price": "1.0023296044093275",
            "percentageChange1hr": "0.00",
            "percentageChange24hr": "-0.25",
            "balance": "16.022686577400921376",
            "contract": "0x55d398326f99059ff775485246999027b3197955"
        }
    ]
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th>Name</th><th>Type</th><th width="178">Description</th><th></th></tr></thead><tbody><tr><td>Success</td><td>Boolean</td><td>Returns true or false for a description</td><td>true</td></tr><tr><td>Data Array</td><td>Array </td><td>Array of Currencies gotten by chainId</td><td></td></tr></tbody></table>

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |
