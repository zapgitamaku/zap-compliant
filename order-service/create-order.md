# Create Order

### POST /v1/orders <a href="#top" id="top"></a>

Allows a User to add a Create an Order on the platform.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to Create an Order.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/orders?isGuest=false
```

### &#x20;**Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

#### For Guests: <a href="#top" id="top"></a>

```
'guest-id: 63e0f4da81979dcc3b9ee123'
```

#### &#x20;**Sample request body for Sell orders (otherCurrency - fiat)** <a href="#top" id="top"></a>

<pre class="language-json"><code class="lang-json"><strong>{
</strong>      "userId": "63e0f4da81979dcc3b9ee123",
<strong>      "amount": 0.01,
</strong>      "marketId": "63e0fd1249be00eb05cad726",
      "refundPublicAccount": "63e0f4da81979dcc3b9ee123",
      "withdrawalBankAccount": "63e0f4da81979dcc3b9ee123",
}
</code></pre>

#### &#x20;**Sample request body for Buy orders (fiat - otherCurrency)** <a href="#top" id="top"></a>

{% hint style="info" %}
**a virtual bank account is created to receive funds**
{% endhint %}

<pre class="language-json"><code class="lang-json"><strong>{
</strong>      "userId": "63e0f4da81979dcc3b9ee123",
<strong>      "amount": 0.01,
</strong>      "marketId": "63e0fd1249be00eb05cad726",
      "refundBankAccount": "63e0f4da81979dcc3b9ee123",
      "withdrawalPublicAccount": "63e0f4da81979dcc3b9ee123",
}
</code></pre>

#### **Sample request body for Swap orders ( otherCurrency - otherCurrency)** <a href="#top" id="top"></a>

<pre class="language-json"><code class="lang-json"><strong>{
</strong>      "userId": "63e0f4da81979dcc3b9ee123",
<strong>      "amount": 0.01,
</strong>      "marketId": "63e0fd1249be00eb05cad726",
      "refundPublicAccount": "63e0f4da81979dcc3b9ee123",
      "withdrawalPublicAccount": "63e0f4da81979dcc3b9ee123",
}
</code></pre>

## &#x20;<a href="#samplerequest" id="samplerequest"></a>

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                              |
| Authorization | This is the ZAP API Platform authorization token, and must be sent with every API request that requires login |
| guest-id      | This is the ID of the Guest                                                                                   |

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="131">Parameter</th><th width="85">Parm Type</th><th width="99">Data Type</th><th width="101">Required</th><th>Description</th></tr></thead><tbody><tr><td>isGuest</td><td>Query</td><td>Boolean</td><td>Optional</td><td>Whether the order is created for a guest or authenticated user<br><br>If isGuest Is true, you can get guestId from socket guestLogin </td></tr><tr><td>Order</td><td>Body</td><td>Order</td><td>Required</td><td>Contains information about Orders on ZAP platform. userId, amount, bankDetailsId and marketId are required.</td></tr></tbody></table>

#### Market Object

Contains information about ZAP's platform orders.

This object is used by the following operations:

* #### POST /v1/orders
* #### GET /v1/orders
* #### GET /v1/orders/:id
* #### PUT /v1/orders/:Id
* #### DELETE /v1/orders/:Id

The properties included in the **Order** object are listed below.

| Property                | Type     | Description                                                                                |
| ----------------------- | -------- | ------------------------------------------------------------------------------------------ |
| id                      | String   | The unique ID for a specific order. Used in Response                                       |
| userId                  | String   | The unique ID of the User.                                                                 |
| amount                  | Number   | The amount the User exchanges.                                                             |
| marketId                | String   | The unique ID for a specific Market.                                                       |
| withdrawalBankAccount   | String   | The unique ID for a user's bank details                                                    |
| depositBankAccount      | Object   | The deposit account number, account name and bankId                                        |
| rate                    | String   | The rate at which the exchange is carried out                                              |
| status                  | String   | The status of the Trade.                                                                   |
| refundPublicAccount     | String   | The account where the refund amount is credited                                            |
| withdrawalPublicAccount | String   | The  account where the Zap sends **otherCurrency** funds to                                |
| depositPublicAccount    | String   | The  account where the user sends **otherCurrency** funds to                               |
| createdAt               | dateTime | This property displays when the currency was created. Used only in response messages.      |
| updatedAt               | dateTime | This property displays when the currency was last updated. Used only in response messages. |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 201, with information about the new bank.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 201 OK
Date: Wed, 25 Jan 2023 23:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response For Sell Order <a href="#top" id="top"></a>

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

### &#x20;<a href="#samplerequest" id="samplerequest"></a>

#### **Sample** Response For Buy Order <a href="#top" id="top"></a>

```json
{
    "success": true,
    "data": {
        "depositBankAccount": {
            "accountNumber": "8223583335",
            "accountName": "ZapTechnologyLi / John Doe",
            "bankId": {
                "name": "SAFE HAVEN MICROFINANCE BANK",
                "sortCode": "090286",
                "icon": "https://res.cloudinary.com/dukdbbrbc/image/upload/v1683650610/image/1683650609169.png",
                "id": "64afd58f177653c33d9a4319"
            }
        },
        "userId": {
            "name": "John Doe",
            "email": "doe@syxlabs.com",
            "emailVerified": true,
            "id": "647dea2605647ed8892e3b0a"
        },
        "amount": 50000,
        "targetAmount": 0.23879566149555082,
        "marketId": {
            "baseCurrencyId": {
                "name": "Nigerian Naira",
                "ticker": "NGN",
                "icon": "https://res.cloudinary.com/dukbcbrbc/image/upload/v16667234892/image/naira.svg",
                "id": "646469e1e3707ac59b49abef"
            },
            "targetCurrencyId": {
                "name": "Ghanian Cedis",
                "ticker": "GHC",
                "icon": "https://res.cloudinary.com/dubdbbrbc/image/upload/v1684298730/image/ghc.svg",
                "id": "646369e1e9284ef59b49abe7"
            },
            "id": "64b99e94aa4317300d03c155"
        },
        "rate": 0.000004775913229911016,
        "status": "pending",
        "withdrawalPublicAccount": "64c007eedab1faccceeab1fadc",
        "expiresAt": "2023-07-25T18:05:25.452Z",
        "createdAt": "2023-07-25T17:35:25.458Z",
        "updatedAt": "2023-07-25T17:35:28.574Z",
        "id": "64c007eedab1faccceeab1fadc"
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

