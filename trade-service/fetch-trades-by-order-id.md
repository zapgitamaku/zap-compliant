# Fetch Trades by Order Id

### GET /api/v1/trade/order/:id <a href="#top" id="top"></a>

Allows a User to get a Trade by OrderId on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to get a trade.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/trades/order/:id
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

| Key | Value  | Description                          |
| --- | ------ | ------------------------------------ |
| Id  | \<Id>  | The unique ID for a specific trade.  |

#### Trade Object

Contains information about ZAP's platform trades.

This object is used by the following operations:

* #### POST /v1/trades
* #### GET /v1/trades
* #### GET /v1/trades/:Id
* #### PUT /v1/trades/:Id
* #### DELETE /v1/trades/:Id

The properties included in the **Trades** object are listed below.

| Property  | Type     | Description                                                                             |
| --------- | -------- | --------------------------------------------------------------------------------------- |
| userId    | string   | The unique ID for a specific user. Required in the request.                             |
| buyTxId   | string   | The  unique ID for buyOrder.                                                            |
| sellTxId  | string   | The unique ID for sellOrder.                                                            |
| createdAt | dateTime | This property displays when the trade was created. Used only in response messages.      |
| updatedAt | dateTime | This property displays when the trade was last updated. Used only in response messages. |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the trades.

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
      data: { trades: 
        "userId": "63d3017b7ef72ecb44f12778",
        "OrderId": "63d3017b7ef72ecb44f1277a",
        "buyTxId": "63d3017b7ef72ecb44f12778",
        "sellTxId": "63d3017b7ef72ecb44f1277a",
        "createdAt": "2023-01-26T01:38:28.848Z",
        "updatedAt": "2023-01-26T01:38:28.848Z",
        "id": "63d3017c7ef72ecb45f2277d"
    }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name  | Type  | Description                                          |
| ----- | ----- | ---------------------------------------------------- |
| Trade | Trade | Contains information about  trades on ZAP  platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 404  | The resource could not be found.                                                                                                                                                                                                                                                                                                  |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |

