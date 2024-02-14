# Delete Trade

### DELETE /v1/trades/:id <a href="#top" id="top"></a>

Allows a User to erase a Trade on the platform.

#### HTTP Method <a href="#top" id="top"></a>

DELETE

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to delete a trade.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/trades/:id
```

#### &#x20;**Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

#### &#x20;**Sample request body** <a href="#top" id="top"></a>

```json
{
      "buyOrderId": "63d3017b7ef72ecb44f1277a",
      "sellOrderId": "63d3017b7ef72ecb44f12778",
}
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

## Request Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="237">Parameter</th><th>Data Type</th><th>Required</th><th>Description</th></tr></thead><tbody><tr><td>Trade</td><td>Trade</td><td>Required</td><td>Contains information about  trades on ZAP platform buyOrderId and sellOrderId are required.</td></tr></tbody></table>



#### Trade Object

Contains information about ZAP's platform bank.

This object is used by the following operations:

* #### POST /v1/trades
* #### GET /v1/trades
* #### GET /v1/trades/:Id
* #### PUT /v1/trades/:Id
* #### DELETE /v1/trades/:Id

The properties included in the **Trade** object are listed below. All properties listed below are **required**

| Property    | Type     | Description                                                                             |
| ----------- | -------- | --------------------------------------------------------------------------------------- |
| id          | string   | The unique ID for a specific user. Required in the request.                             |
| buyOrderId  | string   | The  unique ID for buyOrder.                                                            |
| sellOrderId | string   | The unique ID for sellOrder.                                                            |
| createdAt   | dateTime | This property displays when the trade was created. Used only in response messages.      |
| updatedAt   | dateTime | This property displays when the trade was last updated. Used only in response messages. |

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
  success: true,
      data: "Trade has been deleted successfuly"
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name    | Type | Description                                                 |
| ------- | ---- | ----------------------------------------------------------- |
| Message | Data | Contains information about  deleted trade on ZAP  platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 404  | The resource could not be found.                                                                                                                                                                                                                                                                                                  |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |

