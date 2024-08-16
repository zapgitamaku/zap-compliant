# Fetch Alerts And Watchlist Allowed Tokens

### GET /v1/preferences/tokens <a href="#top" id="top"></a>

Allows a zap user to get the allowed tokens before adding a watchlist or creating an alert on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to get the allowed tokens.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/preferences/tokens
```

#### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                              |
| Authorization | This is the ZAP API Platform authorization token, and must be sent with every API request that requires login |

#### Tokens Object

Contains information about ZAP's platform allowed tokens.

<table><thead><tr><th>Property</th><th width="150">Type</th><th>Description</th></tr></thead><tbody><tr><td>symbol</td><td>string</td><td>The token ticker/symbol.</td></tr><tr><td>icon</td><td>string</td><td>The icon url of the token.</td></tr><tr><td>id</td><td>string</td><td>The unique id of the allowed token and will be used for adding to watchlist or creating price alert.</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the allowed tokens.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Wed, 15 Jun 2024 23:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
    "success": true,
    "data": [
        {
            "symbol": "MATIC",
            "icon": "https://res.cloudinary.com/dukdbbrbc/image/upload/v1712642422/icons/1712642421711.svg",
            "id": "6686c13708a2b18bb2acbd60"
        },
        {
            "symbol": "ARB",
            "icon": "https://res.cloudinary.com/dukdbbrbc/image/upload/v1712753521/icons/1712753522617.svg",
            "id": "6686c13708a2b18bb2acbd61"
        },
        {
            "symbol": "XMR",
            "icon": "https://res.cloudinary.com/dukdbbrbc/image/upload/v1699028552/icons/1699028551057.svg",
            "id": "6686c13708a2b18bb2acbd62"
        },
        {
            "symbol": "OP",
            "icon": "https://res.cloudinary.com/dukdbbrbc/image/upload/v1712753080/icons/1712753081087.svg",
            "id": "6686c13708a2b18bb2acbd63"
        }
    ]
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name  | Type  | Description                                                |
| ----- | ----- | ---------------------------------------------------------- |
| Token | Token | Contains information about allowed tokens on ZAP platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                   |
| ---- | --------------------------------------- |
| 404  | The resource could not be found.        |
| 500  | An error occured processing the request |
