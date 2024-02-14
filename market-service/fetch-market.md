# Fetch Market\*

### GET /v1/markets <a href="#top" id="top"></a>

Allows a User to add a Fetch a list of Markets on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to get markets.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/markets
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

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="237">Parameter</th><th>Parm Type</th><th>Data Type</th><th>Required</th><th>Description</th></tr></thead><tbody><tr><td>Market</td><td>Body</td><td>Market</td><td>Required</td><td>Contains information about  currencies on ZAP platform baseCurrencyId, targetCurrencyId and rate are required.</td></tr></tbody></table>

#### Market Object

Contains information about ZAP's platform currencies.

This object is used by the following operations:

* #### POST /api/v1/market
* #### GET /api/v1/market
* #### GET /api/v1/market/:id
* #### PUT /api/v1/market/:Id
* #### DELETE /api/v1/market/:Id

The properties included in the **Market** object are listed below. All property are **Required**.

| Property         | Type     | Description                                                                                |
| ---------------- | -------- | ------------------------------------------------------------------------------------------ |
| id               | string   | The unique ID for a specific user. Used in Response                                        |
| baseCurrencyId   | string   | The unique ID of the base currency.                                                        |
| targetCurrencyId | string   | The unique ID of the target currency ticker.                                               |
| rate             | Number   | The Exchange rate at the time market was created.                                          |
| createdAt        | dateTime | This property displays when the currency was created. Used only in response messages.      |
| updatedAt        | dateTime | This property displays when the currency was last updated. Used only in response messages. |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the new bank.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Wed, 25 Jan 2023 23:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
    "success": true,
    "data": {
        "marketData": [
            {
                "baseCurrencyId": {
                    "name": "Ghanian Cedis",
                    "ticker": "GHC",
                    "id": "6438a0da6b23108861009e39"
                },
                "targetCurrencyId": {
                    "name": "Nigeian Naira",
                    "ticker": "NGN",
                    "id": "6438a0da6b23108861009e43"
                },
                "createdAt": "2023-04-14T00:39:54.549Z",
                "updatedAt": "2023-04-14T00:39:54.549Z",
                "id": "6438a0da6b23108861009e45"
            },
            {
                "baseCurrencyId": {
                    "name": "United States Dollar",
                    "ticker": "USD",
                    "id": "6438a0da6b23108861009e3a"
                },
                "targetCurrencyId": {
                    "name": "Nigerian Naira",
                    "ticker": "NGN",
                    "id": "6438a0da6b23108861009e43"
                },
                "createdAt": "2023-04-14T00:39:54.549Z",
                "updatedAt": "2023-04-14T00:39:54.549Z",
                "id": "6438a0da6b23108861009e46"
            }
            
        ],
        "bodyLimit": 10,
        "pageLimit": 1,
        "dataCount": 2
    }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name   | Type   | Description                                           |
| ------ | ------ | ----------------------------------------------------- |
| Market | Market | Contains information about  Markets on ZAP  platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                   |
| ---- | --------------------------------------- |
| 404  | The resource could not be found.        |
| 500  | An error occured processing the request |

