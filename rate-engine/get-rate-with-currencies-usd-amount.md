# Get Rate With Currencies(USD amount)

### GET /v1/rateengine/getrate/dollar <a href="#top" id="top"></a>

Allows a User to get the market rate data per volume on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to get the market rate of a market pair.\
The baseCurrencyId and TargetCurrencyId should be gotten from the [Fetch Landing Page Currency](../currency-service/fetch-landingpage-currencies.md)\
The amount should be the amount of baseCurrency to be swapped

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/rateengine/getrate/dollar?baseCurrencyId=646369e1e3707ef59b49abe7&targetCurrencyId=646369e1e3707ef59b49abe6?amount=0.0012
```

```
'Content-Type: application/json'
```





## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header       | Description      |
| ------------ | ---------------- |
| Content-type | application/json |

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="261">Parameter</th><th>Parm Type</th><th>Data Type</th><th>Required</th><th>Description</th></tr></thead><tbody><tr><td>baseCurrencyId</td><td>Query</td><td>String</td><td>Required</td><td>base currency Id: </td></tr><tr><td>targetCurrencyId</td><td>Query</td><td>String</td><td>Required</td><td>target currency Id: </td></tr><tr><td>amount</td><td>Query</td><td>String</td><td>Required</td><td>base amount in dollar</td></tr></tbody></table>

#### Rate Object

Contains information about ZAP's platform rate data.

This object is used by the following operations:

* #### GET /v1/rateengine/getrate/



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
        "marketId": "64c13d0ec5efabf7529bfa79"},
        "rate": 840.8157355709101,
        "minAmount": 1.0109230406146643,
        "maxAmount": 10109.230406146644,
        "baseCurrencyToUsdRate": 0.9991868515400001,
        "targetCurrencyToUsdRate": 0.0001868515400001,
        "fees": 22.999
    }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name | Type      | Description                                               |
| ---- | --------- | --------------------------------------------------------- |
| Rate | rate Data | Contains information about  Market Rate on ZAP  platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 401  | Unauthorized                                                                                                                                                                                                                                                                                                                      |
| 404  | Not Found: Returned if the request                                                                                                                                                                                                                                                                                                |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |

