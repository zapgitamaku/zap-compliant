# Fetch Orders By User Id with filter

### GET /v1/orders/user/:userId?query <a href="#top" id="top"></a>

Allows a User to fetch order by userId on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to get orders by currency Id.

#### **Sample request** URL with query params <a href="#top" id="top"></a>

```
https://{hostname}/v1/orders/user/:userId
?marketId=marketId1,marketId2,marketId3
&bankId=bankId1,bankId2
&currencyId=currencyId1,currencyId2
&createdAt.start=2023-05-01
&createdAt.end=2023-05-04
&status=verified



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

#### **Sample request query** <a href="#top" id="top"></a>

<table><thead><tr><th width="203">Key</th><th width="209">Value</th><th>Description</th></tr></thead><tbody><tr><td>marketId</td><td>id, array of ids</td><td>Optional query parameter that specifies the marketId in the filter of the order in the response body</td></tr><tr><td>currencyId</td><td>id, array of ids</td><td>Optional query parameter that specifies the currencyId in the filter of the order in the response body</td></tr><tr><td>bankId</td><td>id, array of ids</td><td>Optional query parameter that specifies the bankId in the filter of the order in the response body</td></tr><tr><td>createdAt.start</td><td>date</td><td>Optional query parameter that adds a start date range to filter of the order in the response body</td></tr><tr><td>createdAt.end</td><td>date</td><td>Optional query parameter that adds an end date range to filter of the order in the response body</td></tr><tr><td>status</td><td>string</td><td>Optional query parameter that adds a status to the filter of orders in the response body</td></tr></tbody></table>



## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the orders.

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
        "updatedAt": "2023-07-22T08:40:25.434Z",
        "depositPublicAccount": "64bb95f7eeb410a6358b0c29",
        "id": "64bb95f7eeb410a6358b0c29"
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

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                   |
| ---- | --------------------------------------- |
| 404  | The resource could not be found.        |
| 500  | An error occured processing the request |

