# Create Price Alert

### POST /v1/priceAlerts <a href="#top" id="top"></a>

Allows the zap user to Create a new price alert for a token.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to Create a new price alert.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/priceAlerts
```

#### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

#### **Sample request body** <a href="#top" id="top"></a>

```json
{
   "userId": "6515a38ef6d2985656496941",
   "token": "6686c13708a2b18bb2acbd58",
   "duration": "recurrent", // required
   "percentageChange": 3, // optional
   "percentageChangeType": "down" // optional "up" or "down"
    "amountChange": 250,  // optional
    "amountChangeType": "above" // optional "above" or "below"
    "recurrentDuration": 120 // should be in minutes format so 120 is 2hrs
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                              |
| Authorization | This is the ZAP API Platform authorization token, and must be sent with every API request that requires login |

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="178">Parameter</th><th width="98">Parm Type</th><th width="116">Required</th><th>Description</th></tr></thead><tbody><tr><td>PriceAlert</td><td>Body</td><td>Required</td><td>Contains information about a new price alert on ZAP platform. userId, token, duration are required. percentageChange, percentageChangeType, amountChange, amountChangeType are optional and recurrentDuration is required if duration is recurrent.</td></tr></tbody></table>

#### PriceAlert Object

Contains information about ZAP's platform price alert.

The properties included in the PriceAlert object are listed below.

<table><thead><tr><th>Property</th><th width="132">Type</th><th>Description</th></tr></thead><tbody><tr><td>userId</td><td>string</td><td>The unique id of the user</td></tr><tr><td>token</td><td>string</td><td>The token ticker/symbol</td></tr><tr><td>duration</td><td>string</td><td>The duration of the price alert</td></tr><tr><td>percentageChange</td><td>number</td><td>The percentage change required for token price alert</td></tr><tr><td>percentageChangeType</td><td>string</td><td>The type of the percentage change. Enum "up" or "down"</td></tr><tr><td>amountChange</td><td>number</td><td>The amount change required for token price alert</td></tr><tr><td>amountChangeType</td><td>string</td><td>The amount change type. Enum "above" and "below"</td></tr><tr><td>recurrentDuration</td><td>number</td><td>The duration of the recurrent in minutes conversion</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 201, with information about the new price alert.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 201 OK
Date: Wed, 15 Aug 2024 23:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
    "success": true,
    "data": {
        "userId": "6515a38ef6d2985656496941",
        "token": {
            "lastPrice": "93902125.72194728",
            "usdPrice": "57242.67564348196",
            "symbol": "BTC",
            "priceChangePercent": "0.72",
            "percentChange1hr": "0.72",
            "percentChange24hr": "0.71",
            "marketCap": "1180672875219",
            "volume": "26279321972",
            "history": [],
            "icon": "https://res.cloudinary.com/dukdbbrbc/image/upload/v1684235118/image/btc.svg",
            "createdAt": "2024-07-04T15:35:19.200Z",
            "updatedAt": "2024-08-16T06:27:15.765Z",
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
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name       | Type       | Description                                                     |
| ---------- | ---------- | --------------------------------------------------------------- |
| PriceAlert | PriceAlert | Contains information about the new price alert on ZAP platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |
