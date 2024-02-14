# Fill Order by Id

### POST /v1/orders/fill/:id <a href="#top" id="top"></a>

Allows a Payout Admin to fill an existing order on the platform.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to fill an existing order on the platform.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/orders/fill/:Id
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

## Request Query <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="123">Parameter</th><th width="125">Parm Type</th><th width="114">Required</th><th></th></tr></thead><tbody><tr><td>id</td><td>&#x3C;id></td><td>Required</td><td>The unique ID for a specific order. </td></tr></tbody></table>

## Request Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="125">Key</th><th>Value</th><th>Description</th></tr></thead><tbody><tr><td>txreceipt</td><td>String</td><td>Contains the ReferenceId from the bank transaction</td></tr><tr><td>bankId</td><td>string</td><td>Contains the bankId of the payout bank</td></tr></tbody></table>

#### **Sample request body** <a href="#top" id="top"></a>

```json
{
        "txReceipt": "000003230522145274002245289391",
        "bankId": "646ff552299a63ef70e48ccc",
}
```

#### Order Object

Contains information about ZAP's platform order.

This object is used by the following operations:

* #### POST /v1/orders
* #### GET /v1/orders
* #### GET /v1/orders/:id
* #### PUT /v1/orders/:Id
* #### DELETE /v1/orders/:Id

The properties included in the **Order** object are listed below. All property are **Optional**.

| Property              | Type     | Description                                                                                |
| --------------------- | -------- | ------------------------------------------------------------------------------------------ |
| id                    | String   | The unique ID for a specific order. Used in Response                                       |
| userId                | String   | The unique ID of the User.                                                                 |
| amount                | Number   | The amount the User exchanges.                                                             |
| marketId              | String   | The unique ID for a specific Market.                                                       |
| withdrawalBankAccount | String   | The unique ID for a user's bank details                                                    |
| depositBankAccount    | Object   | The deposit account number, account name and bankId                                        |
| rate                  | String   | The rate at which the exchange is carried out                                              |
| status                | String   | The status of the order.                                                                   |
| refundPublicKey       | String   | The public address where the refund amount is credited                                     |
| withdrawalPublicKey   | String   | The public address where the Zap sends crypto funds to                                     |
| depositPublicKey      | String   | The public address where the user sends crypto funds to                                    |
| createdAt             | dateTime | This property displays when the currency was created. Used only in response messages.      |
| updatedAt             | dateTime | This property displays when the currency was last updated. Used only in response messages. |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the updated order.

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
    "data": "Order filled and trade updated successfully"
}

```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name  | Type  | Description                                          |
| ----- | ----- | ---------------------------------------------------- |
| Order | Order | Contains information about  Orders on ZAP  platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |

