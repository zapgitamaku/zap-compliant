# Fetch Specific Currency Price Feed History and Detail

### GET /v1/rateengine/pricefeed/:ticker <a href="#top" id="top"></a>

Allows a User to get the price feed historical data for a specific currency by ticker on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to get the currency price feed history.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/rateengine/priceFeed/:ticker
```

#### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header       | Description      |
| ------------ | ---------------- |
| Content-type | application/json |

#### Price Feed Object

Contains information about ZAP's platform priceFeed data.

This object is used by the following operations:

* **GET /v1/rateengine/priceFeed/:ticker**

The properties included in the **Rate** object are listed below.

| Property | Type       | Description                                |
| -------- | ---------- | ------------------------------------------ |
| data     | Price Feed | The price feed data for specific currency. |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the currency price feed data.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Tue, 28 Jun 2024 02:10:15 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
    "success": true,
    "data": {
        "currencyDetail": {
            "name": "DAI",
            "ticker": "DAI",
            "chainId": "1",
            "isCrypto": true,
            "createdAt": "2023-11-03T15:46:29.509Z",
            "updatedAt": "2024-06-24T16:13:53.562Z",
            "icon": "https://res.cloudinary.com/dukdbbrbc/image/upload/v1699028669/icons/1699028667964.svg",
            "chainIcon": "https://res.cloudinary.com/dukdbbrbc/image/upload/v1684235469/image/ether.svg",
            "network": "Ethereum",
            "description": "Dai is a decentralized stablecoin that is soft-pegged to the US Dollar, maintained by the MakerDAO system of smart contracts on the Ethereum blockchain. Unlike other stablecoins, Dai is not backed by fiat currency but by collateral in the form of other cryptocurrencies.",
            "explorer": "https://etherscan.io/token/0x6b175474e89094c44da98b954eedeac495271d0feet",
            "twitter": "https://twitter.com/MakerDAO",
            "website": "https://makerdao.com/",
            "id": "654515d527ff258a368d1627"
        },
        "history": [
            {
                "date": 1514352600000,
                "rate": 0.978816,
                "volume": 966318,
                "cap": null,
                "liquidity": null
            },
            {
                "date": 1518457200000,
                "rate": 1.005,
                "volume": 11486,
                "cap": 14492200,
            },
            {
                "date": 1612863000000,
                "rate": 1.0006680972280404,
                "volume": 251077691,
                "cap": 858843244,
                "liquidity": 19699343
            },
    }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name       | Type            | Description                                                                        |
| ---------- | --------------- | ---------------------------------------------------------------------------------- |
| Price Feed | price feed Data | Contains information about Historical Prices of a specific Zap supported currency. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 401  | Unauthorized                                                                                                                                                                                                                                                                                                                      |
| 404  | Not Found: Returned if the request                                                                                                                                                                                                                                                                                                |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |
