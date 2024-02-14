# Get Rate

### GET /v1/rateengine/getrate/:marketId <a href="#top" id="top"></a>

Allows a User to get the market rate data on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to get the market rate.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/rateengine/getrate/:marketId?amount=amount
```

#### &#x20;**Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```





## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                              |
| Authorization | This is the ZAP API Platform authorization token, and must be sent with every API request that requires login |

## Request  <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="231">Parameter</th><th>Parm Type</th><th>Data Type</th><th>Required</th><th>Description</th></tr></thead><tbody><tr><td>marketID</td><td>param</td><td>String</td><td>Required</td><td>Contains information about  Markets data on ZAP platform MarketId is required.</td></tr><tr><td>amount</td><td>query</td><td>string/number</td><td>Required</td><td>Amount to be swapped</td></tr></tbody></table>

#### Rate Object

Contains information about ZAP's platform rate data.

This object is used by the following operations:

* #### POST /v1/rateengine/getrate/:marketId



The properties included in the **Rate** object are listed below.

| Property | Type  | Description      |
| -------- | ----- | ---------------- |
| data     | Float | The market rate. |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the market rate.

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
    "data": {
         "rate": 0.000004775913229911016,
         "minAmount": 876.2886597938146,
         "maxAmount": 8762886.597938146,
         "baseCurrencyToUsdRate": 0.001176470588235294,
         "fees": 0.001
    }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name      | Type      | Description                                               |
| --------- | --------- | --------------------------------------------------------- |
| Rate      | rate Data | Contains information about  Market Rate on ZAP  platform. |
| rate      | Number    | Conversion rate for the particular market in Naira        |
| minAmount | Number    | minimum amount that can be processed by our providers     |
| usdRate   | Number    | 1 USD to Naira                                            |
| fees      | Number    | The fees charged on the order                             |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 401  | Unauthorized                                                                                                                                                                                                                                                                                                                      |
| 404  | Not Found: Returned if the request                                                                                                                                                                                                                                                                                                |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |

