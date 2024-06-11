# Price Feed

### GET /v1/rateengine/priceFeed <a href="#top" id="top"></a>

Allows a User to get the price feed data on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to get the price.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/rateengine/priceFeed
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

* **GET /v1/rateengine/priceFeed**

The properties included in the **Rate** object are listed below.

| Property | Type       | Description                                    |
| -------- | ---------- | ---------------------------------------------- |
| data     | Price Feed | The price feed data for ssupported currencies. |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the price feed data.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Tue, 28 Feb 2023 02:10:15 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
    "success": true,
    "data": [
            {"lastPrice": "2965.157296583584",
            "usdPrice": 2.11043223956127,
            "symbol": "OP",
            "icon": "https://res.cloudinary.com/dukdbbrbc/image/upload/v1712753080/icons/1712753081087.svg",
            "priceChangePercent": "-0.34",
            "percentChange1hr": "-0.34",
            "percentChange24hr": "-5.90",
            "marketCap": 2293807618,
            "volume": 387118081,
            "allTimeHighUsd": 4.855611043091424,
            "currencyDetail": {
                "name": "Optimism",
                "ticker": "OP",
                "chainId": "10",
                "chainIcon": "https://res.cloudinary.com/dukdbbrbc/image/upload/v1712753080/icons/1712753081087.svg",
                "isCrypto": true,
                "network": "Optimism",
                "icon": "https://res.cloudinary.com/dukdbbrbc/image/upload/v1712753080/icons/1712753081087.svg",
                "createdAt": "2024-04-12T12:14:22.060Z",
                "updatedAt": "2024-04-12T12:14:22.060Z",
                "id": "6619259e0015d8a3e6d37e52"
            },
            "history": [
                {
                    "date": 1654680600000,
                    "rate": 0.9869152728903903,
                    "volume": 188127712,
                    "cap": 211938440,
                    "liquidity": 3848072
                },
                {
                    "date": 1655321400000,
                    "rate": 0.5417595036493404,
                    "volume": 144455239,
                    "cap": 116341967,
                    "liquidity": 5397813
                },
                {
                    "date": 1655962200000,
                    "rate": 0.47873223348679317,
                    "volume": 44521049,
                    "cap": 102806964,
                    "liquidity": 7693701
                }
            ]
        }]
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name       | Type            | Description                                                             |
| ---------- | --------------- | ----------------------------------------------------------------------- |
| Price Feed | price feed Data | Contains information about Prices of Zap supported currencies in Naira. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 401  | Unauthorized                                                                                                                                                                                                                                                                                                                      |
| 404  | Not Found: Returned if the request                                                                                                                                                                                                                                                                                                |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |
