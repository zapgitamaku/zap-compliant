# Delete Market by Id

### DELETE /v1/markets/:id <a href="#top" id="top"></a>

Allows a User to erase a Market on the platform.

#### HTTP Method <a href="#top" id="top"></a>

DELETE

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to erase a Market.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/markets/:Id
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

#### Market Object

Contains information about ZAP's platform currencies.

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
| createdAt        | dateTime | This property displays when the currency was created. Used only in response messages.      |
| updatedAt        | dateTime | This property displays when the currency was last updated. Used only in response messages. |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about success of the deletion.

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
        "baseCurrencyId": "63d40d8e3272a7c06012736d",
        "targetCurrencyId": "63d40d8e3272a7c06012736f",
        "createdAt": "2023-01-27T17:44:46.596Z",
        "updatedAt": "2023-01-27T18:03:22.994Z",
        "id": "63d40d8e3272a7c060147372"
      }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name    | Type   | Description                                                |
| ------- | ------ | ---------------------------------------------------------- |
| Message | Status | Contains information about  the Deletion on ZAP  platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |

