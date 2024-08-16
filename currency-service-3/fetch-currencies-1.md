# Fetch Specific User Preference

### GET /v1/preferences/:userId <a href="#top" id="top"></a>

Allows a zap user to get their alert is toggled on/off and watchlist settings on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to get a user preference document.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/preferences/:userId
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

#### UserPreference Object

Contains information about ZAP's platform allowed tokens.

<table><thead><tr><th>Property</th><th width="150">Type</th><th>Description</th></tr></thead><tbody><tr><td>userId</td><td>string</td><td>The unique id of the user.</td></tr><tr><td>allowedTokenWatchlist</td><td>boolean</td><td>It specifies if the user has toggled on/off the watchlist feature </td></tr><tr><td>allowedPriceAlert</td><td>boolean</td><td>It specifies if the user has toggled on/off the price alert feature </td></tr><tr><td>watchListTokens</td><td>array of string </td><td>It contains the tokens id the user has added to the watchlist</td></tr><tr><td>watchListPercentageChange</td><td>number</td><td>The percentage change range for the tokens in the watchListTokens array.</td></tr></tbody></table>

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
    "data": {
        "userId": "6515a38ef6d2985656496941",
        "allowTokenWatchList": true,
        "watchListTokens": [
            {
                "lastPrice": "229255.59898938856",
                "usdPrice": "140.32378623460733",
                "symbol": "SOL",
                "priceChangePercent": "0.96",
                "percentChange1hr": "0.96",
                "percentChange24hr": "0.15",
                "marketCap": "68168474376",
                "volume": "3161741900",
                "history": [],
                "icon": "https://res.cloudinary.com/dukdbbrbc/image/upload/v1704295321/icons/1704295319104.svg",
                "createdAt": "2024-07-04T15:35:19.202Z",
                "updatedAt": "2024-08-16T06:27:17.036Z",
                "allTimeHighUsd": "259.8360337991446",
                "name": "Solana",
                "id": "6686c13708a2b18bb2acbd5c"
            }
        ],
        "watchListPercentageChange": 5,
        "allowPriceAlert": false,
        "createdAt": "2024-08-16T07:35:22.113Z",
        "updatedAt": "2024-08-16T07:35:22.113Z",
        "id": "66bf013ab4a47c0955a312d1"
    }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name           | Type           | Description                                                 |
| -------------- | -------------- | ----------------------------------------------------------- |
| UserPreference | UserPreference | Contains information about user preference on ZAP platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                   |
| ---- | --------------------------------------- |
| 404  | The resource could not be found.        |
| 500  | An error occured processing the request |
