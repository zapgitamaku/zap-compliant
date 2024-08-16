# Update Create Price Alert

### PUT /v1/priceAlerts <a href="#top" id="top"></a>

Allows the zap user to Create a new price alert for a token.

#### HTTP Method <a href="#top" id="top"></a>

PUT

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
   "alertId": "6515a38ef6d2985656496941",
   "token": "6686c13708a2b18bb2acbd58", // optional
   "duration": "recurrent", // optional
   "percentageChange": 3, // optional
   "percentageChangeType": "down" // optional
    "amountChange": 250,  // optional
    "amountChangeType": "above" // optional
    "recurrentDuration": 120 // should be in minutes format so 120 is 2hrs
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                              |
| Authorization | This is the ZAP API Platform authorization token, and must be sent with every API request that requires login |

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="178">Parameter</th><th width="98">Parm Type</th><th width="116">Required</th><th>Description</th></tr></thead><tbody><tr><td>PriceAlert</td><td>Body</td><td>Required</td><td>Contains information about a new price alert on ZAP platform. alertId is  required, rest are optional and recurrentDuration is required if duration is recurrent.</td></tr></tbody></table>

#### PriceAlert Object

Contains information about ZAP's platform price alert.

The properties included in the PriceAlert object are listed below.

<table><thead><tr><th>Property</th><th width="132">Type</th><th>Description</th></tr></thead><tbody><tr><td>userId</td><td>string</td><td>The unique id of the user</td></tr><tr><td>preferenceId</td><td>string</td><td>The unique id of the user preference</td></tr><tr><td>token</td><td>string</td><td>The token ticker/symbol</td></tr><tr><td>duration</td><td>string</td><td>The duration of the price alert</td></tr><tr><td>percentageChange</td><td>number</td><td>The percentage change required for token price alert</td></tr><tr><td>percentageChangeType</td><td>string</td><td>The type of the percentage change.</td></tr><tr><td>amountChange</td><td>number</td><td>The amount change required for token price alert</td></tr><tr><td>amountChangeType</td><td>string</td><td>The amount change type</td></tr><tr><td>recurrentDuration</td><td>number</td><td>The duration of the recurrent in minutes conversion</td></tr></tbody></table>

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
    "data": "Alert updated successfully"
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
