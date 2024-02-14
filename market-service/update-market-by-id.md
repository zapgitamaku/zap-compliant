# Update Market by Id

### PUT /v1/markets/:id <a href="#top" id="top"></a>

Allows a User to add a modify an existing Market on the platform.

#### HTTP Method <a href="#top" id="top"></a>

PUT

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to Create a Market.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/markets/:Id
```

#### &#x20;**Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

#### &#x20;**Sample request body** <a href="#top" id="top"></a>

```json
{
    "baseCurrencyId": "63d40d8e3272a7c06012736d",
    "targetCurrencyId": "63d40d8e3272a7c06012736f",
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                              |
| Authorization | This is the ZAP API Platform authorization token, and must be sent with every API request that requires login |

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="237">Parameter</th><th>Parm Type</th><th>Data Type</th><th>Required</th><th>Description</th></tr></thead><tbody><tr><td>Market</td><td>Body</td><td>Market</td><td>Required</td><td>Contains information about  currencies on ZAP platform baseCurrencyId, targetCurrencyId and rate are required.</td></tr></tbody></table>

#### Market Object

Contains information about ZAP's platform Markets.

This object is used by the following operations:

* #### POST /v1/markets
* #### GET /v1/markets
* #### GET /v1/markets/:id
* #### PUT /v1/markets/:Id
* #### DELETE /v1/markets/:Id

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

If successful, this operation returns HTTP status code 200, with information about the updated market.

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
    success: true,
     data: {
      "baseCurrencyId": { 
          "name": "Bitcoin", 
          "ticker": "BTC", 
          "id": "63d40d8e3272a7c06012736d" 
        },
      "targetCurrencyId": {
          "name": "US Dollar",
          "ticker": "USD",
          "id": "63d40d8e3272a7c06012736f"
        },
      "createdAt": "2023-01-27T17:53:58.765Z",
      "updatedAt": "2023-01-27T17:53:58.765Z",
      "id": "63d40ab60b2b2cb18219704f"
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

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |

