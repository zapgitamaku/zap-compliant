# Logic for Expired Order by Id

### POST /v1/orders/expired/:id <a href="#top" id="top"></a>

Allows a User to interact with  an expired order to be processed/ refunded on the platform.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request for a process/refund of an order on the platform.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/orders/expired/:Id
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

<table><thead><tr><th width="137">Parameter</th><th width="130">Parm Type</th><th width="114">Required</th><th></th></tr></thead><tbody><tr><td>id</td><td>&#x3C;id></td><td>Required</td><td>The unique ID for a specific order. </td></tr></tbody></table>

## Request Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="192">Key</th><th>Value</th><th>Description</th></tr></thead><tbody><tr><td>hash</td><td>Hash</td><td>Contains the hash received from the socket and is required.</td></tr><tr><td>refundDifference</td><td>Boolean</td><td>it is required.</td></tr><tr><td>processOrder</td><td>Boolean</td><td>it is required.</td></tr></tbody></table>

#### **Sample request body** <a href="#top" id="top"></a>

```json
{
  "hash": "0xbf1D43fD093E76c097C869bA21fB2c7B59440521",
  "refundDifference": true,
  "processOrder": true,
}
```

Note: If order is expired and user sends funds, they should be able to still either process their order  or request a refund.\
\
If they request a refund, the processOrder must be false.\
If they choose to process the order, they still have the option to refund the difference if they overpaid. So the refundDifference will either be true or false

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
| status                | String   | The status of the Trade.                                                                   |
| refundPublicKey       | String   | The public address where the refund amount is credited                                     |
| withdrawalPublicKey   | String   | The public address where the Zap sends crypto funds to                                     |
| depositPublicKey      | String   | The public address where the user sends crypto funds to                                    |
| createdAt             | dateTime | This property displays when the currency was created. Used only in response messages.      |
| updatedAt             | dateTime | This property displays when the currency was last updated. Used only in response messages. |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the order.

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
     // if successfull the data might also be undefined
    "data": "Order refunded"
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

