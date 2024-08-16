# Fetch Specific User Token Alerts

### GET /v1/priceAlerts/token/:userId?ticker=ARB <a href="#top" id="top"></a>

Allows a zap user to get all their alerts for a particular token on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to get a user alerts for a token.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/priceAlerts/token/:userId?ticker=ARB
```

#### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                              |
| Authorization | This is the ZAP API Platform authorization token, and must be sent with every API request that requires login |

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="163">key</th><th width="173">value</th><th>Description</th></tr></thead><tbody><tr><td>userId</td><td>&#x3C;userid></td><td>The unique ID of the user.</td></tr></tbody></table>

#### PriceAlert Object

Contains information about ZAP's platform price alert.

The properties included in the PriceAlert object are listed below.

<table><thead><tr><th>Property</th><th width="132">Type</th><th>Description</th></tr></thead><tbody><tr><td>userId</td><td>string</td><td>The unique id of the user</td></tr><tr><td>token</td><td>string</td><td>The token id</td></tr><tr><td>duration</td><td>string</td><td>The duration of the price alert</td></tr><tr><td>percentageChange</td><td>number</td><td>The percentage change required for token price alert</td></tr><tr><td>percentageChangeType</td><td>string</td><td>The type of the percentage change.</td></tr><tr><td>amountChange</td><td>number</td><td>The amount change required for token price alert</td></tr><tr><td>amountChangeType</td><td>string</td><td>The amount change type</td></tr><tr><td>recurrentDuration</td><td>number</td><td>The duration of the recurrent in minutes conversion</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the user preferences.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Wed, 15 Jun 2024 23:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
    "success": true,
    "data": [
        {
            "userId": "6515a38ef6d2985656496941",
            "token": {
                "lastPrice": "93902125.72194728",
                "usdPrice": "58566.86306755906",
                "symbol": "BTC",
                "priceChangePercent": "0.72",
                "percentChange1hr": "0.72",
                "percentChange24hr": "0.71",
                "marketCap": "1180672875219",
                "volume": "26279321972",
                "history": [],
                "icon": "https://res.cloudinary.com/dukdbbrbc/image/upload/v1684235118/image/btc.svg",
                "createdAt": "2024-07-04T15:35:19.200Z",
                "updatedAt": "2024-08-16T08:00:00.815Z",
                "allTimeHighUsd": "73781.24185982272",
                "name": "Bitcoin",
                "id": "6686c13708a2b18bb2acbd58"
            },
            "duration": "oneTime",
            "oneTimeNotified": false,
            "percentageChange": 3,
            "percentageChangeType": "down",
            "tokenPrice": 0,
            "amountChange": null,
            "amountChangeType": null,
            "active": true,
            "createdAt": "2024-08-16T07:54:22.111Z",
            "updatedAt": "2024-08-16T07:54:22.111Z",
            "id": "66bf05aeb1e460d576c1bc81"
        }
    ]
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name        | Type        | Description                                                 |
| ----------- | ----------- | ----------------------------------------------------------- |
| PriceAlerts | PriceAlerts | Contains information about user preference on ZAP platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                   |
| ---- | --------------------------------------- |
| 404  | The resource could not be found.        |
| 500  | An error occured processing the request |
