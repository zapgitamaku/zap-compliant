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

#### &#x20;**Sample request headers** <a href="#top" id="top"></a>

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

* #### GET /v1/rateengine/priceFeed



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
        {
            "lastPrice": 193511.989948944,
            "symbol": "BNBBSC",
            "icon": "https://res.cloudinary.com/dukdbbrbc/image/upload/v1684235730/image/bnb.svg",
            "priceChangePercent": "0.09507276760095486"
        },
        {
            "lastPrice": 23975153.599999998,
            "symbol": "BTC",
            "icon": "https://res.cloudinary.com/dukdbbrbc/image/upload/v1684235118/image/btc.svg",
            "priceChangePercent": "-0.016647799160966457"
        },
        {
            "lastPrice": 799.78147152,
            "symbol": "USDTBSC",
            "icon": "https://res.cloudinary.com/dukdbbrbc/image/upload/v1684235224/image/tether.svg",
            "priceChangePercent": "0.016778787339467065"
        },
        {
            "lastPrice": 1517230.011099576,
            "symbol": "ETH",
            "icon": "https://res.cloudinary.com/dukdbbrbc/image/upload/v1684235469/image/ether.svg",
            "priceChangePercent": "0.05435677888048291"
        },
        {
            "lastPrice": 794.477065336,
            "symbol": "USDTERC20",
            "icon": "https://res.cloudinary.com/dukdbbrbc/image/upload/v1684235224/image/tether.svg",
            "priceChangePercent": "0.01661162510549459"
        }
    ]
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name       | Type            | Description                                                              |
| ---------- | --------------- | ------------------------------------------------------------------------ |
| Price Feed | price feed Data | Contains information about  Prices of Zap supported currencies in Naira. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 401  | Unauthorized                                                                                                                                                                                                                                                                                                                      |
| 404  | Not Found: Returned if the request                                                                                                                                                                                                                                                                                                |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |

