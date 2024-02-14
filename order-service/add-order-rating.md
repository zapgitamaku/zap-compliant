# Add Order Rating

### PUT /v1/orders/rating/:id <a href="#top" id="top"></a>

Allows a zap user and guest to give rating about their processed orders .

#### HTTP Method <a href="#top" id="top"></a>

PUT

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request for a zap user and guest to give rating about their orders.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/orders/rating/:id
```

### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

#### For Guests: <a href="#top" id="top"></a>

```
'guest-id: 63e0f4da81979dcc3b9ee123'
```

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="154">Key</th><th width="128">Value</th><th>Description</th></tr></thead><tbody><tr><td>Id</td><td>&#x3C;Id> </td><td>The unique ID for an order. make sure the guest/user making this rating is the creator of the order. </td></tr></tbody></table>

#### &#x20;**Sample request body** <a href="#top" id="top"></a>

```json
{
    "comment": "nice and fast trading",
    "rating": 4
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                              |
| Authorization | This is the ZAP API Platform authorization token, and must be sent with every API request that requires login |
| guest-id      | This is the Id of the Guest                                                                                   |

## Request Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="129">Parameter</th><th width="99">Parm Type</th><th width="100">Data Type</th><th width="99">Required</th><th>Description</th></tr></thead><tbody><tr><td>Order</td><td>Body</td><td>Order</td><td>Optional</td><td>Contains information about  orders rating.<br>All fields are optional</td></tr></tbody></table>

#### Order Object

Contains information about ZAP's platform order.

The properties included in the **Order** object are listed below. All property are **Optional**.

| Property                | Type     | Description                                                                             |
| ----------------------- | -------- | --------------------------------------------------------------------------------------- |
| id                      | String   | The unique ID for a specific order. Used in Response                                    |
| userId                  | String   | The unique ID of the User.                                                              |
| amount                  | Number   | The amount the User exchanges.                                                          |
| marketId                | String   | The unique ID for a specific Market.                                                    |
| withdrawalBankAccount   | String   | The unique ID for a user's bank details                                                 |
| depositBankAccount      | Object   | The deposit account number, account name and bankId                                     |
| rate                    | String   | The rate at which the exchange is carried out                                           |
| status                  | String   | The status of the order.                                                                |
| refundPublicAccount     | String   | The account where the refund amount is credited                                         |
| withdrawalPublicAccount | String   | The account where the Zap sends otherCurrency funds to                                  |
| depositPublicAccount    | String   | The account where the user sends otherCurrency funds to                                 |
| createdAt               | dateTime | This property displays when the order was created. Used only in response messages.      |
| updatedAt               | dateTime | This property displays when the order was last updated. Used only in response messages. |

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
      "data": {
        "userId": {
            "name": "John Doe",
            "email": "Doe@syxlabs.com",
            "emailVerified": true,
            "id": "647dea778238489ed1d5193b0a"
        },
        "amount": 10,
        "targetAmount": 8272.8482269116,
        "marketId": {
            "baseCurrencyId": {
                "name": "United States Dollar",
                "ticker": "USD",
                "icon": "https://res.cloudinary.com/dukkxbrbc/image/upload/v1684773224/image/usd.svg",
                "id": "646369e1e9901ef59b49abea"
            },
            "targetCurrencyId": {
                "name": "Nigerian Naira",
                "ticker": "NGN",
                "icon": "https://res.cloudinary.com/dutxbbrbc/image/upload/v1684998892/image/naira.svg",
                "id": "646369e1e9981ef99b49abef"
            },
            "id": "646369e1e7123ef59b49abf8"
        },
        "withdrawalBankAccount": {
            "bankId": {
                "name": "OPAY",
                "sortCode": "100004",
                "icon": "https://res.cloudinary.com/dukdbbrbc/image/upload/v1683650610/image/1683650609169.png",
                "id": "64afd58f177653c09d9a42f7"
            },
            "accountNumber": "8108681918",
            "accountName": "DAVID UGOCHUKWU AMAKU",
            "id": "64afdbf6ca8768ec953e3bf0e"
        },
        "rate": 827.28482269116,
        "status": "pending",
        "refundPublicAccount": "64bb95f7eeb410a6358b0c29",
        "expiresAt": "2023-07-22T09:10:23.526Z",
        "createdAt": "2023-07-22T08:40:23.540Z",
        "comment": "nice and fast trading",
        "rating": 3.5,
        "id": "651ffac935d82d97e2a595d8"
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
| Order | Order | Contains information about  Orders on ZAP  platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |

