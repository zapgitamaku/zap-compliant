# Refund Order by Id

### POST /v1/orders/refund/:id <a href="#top" id="top"></a>

Allows a User to request a refund for an existing order on the platform.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request for a refund of an existing order on the platform.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/orders/refund/:Id
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

#### &#x20;<a href="#top" id="top"></a>



## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                              |
| Authorization | This is the ZAP API Platform authorization token, and must be sent with every API request that requires login |
| guest-id      | This is the Id of the Guest                                                                                   |

## Request Query <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="123">Parameter</th><th width="125">Parm Type</th><th width="114">Required</th><th></th></tr></thead><tbody><tr><td>id</td><td>&#x3C;id></td><td>Required</td><td>The unique ID for a specific order. </td></tr></tbody></table>

## Request Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="125">Key</th><th>Value</th><th>Description</th></tr></thead><tbody><tr><td>hash</td><td>Hash</td><td>Contains the hash received from the socket and is required.</td></tr></tbody></table>

#### Order Object

Contains information about ZAP's platform order.

This object is used by the following operations:

* #### POST /v1/orders
* #### GET /v1/orders
* #### GET /v1/orders/:id
* #### PUT /v1/orders/:Id
* #### DELETE /v1/orders/:Id

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
    // if successfull the data might also be undefined
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

<table><thead><tr><th width="235.33333333333331">Name</th><th>Type</th><th>Description</th></tr></thead><tbody><tr><td>Order</td><td>Order</td><td>Contains information about  Orders on ZAP  platform.</td></tr></tbody></table>

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |

