# Validate Wallet Address

### POST /v1/orders/validateAddress <a href="#top" id="top"></a>

Allows validation of a zap user receiving wallet address  on the platform.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to validate a zap user receiving wallet address on the platform.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/orders/validateAddress
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

## Request Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="125">Key</th><th>Value</th><th>Description</th></tr></thead><tbody><tr><td>ticker</td><td>String</td><td>The target currency ticker</td></tr><tr><td>address</td><td>string</td><td>Contains the receiving wallet address of the zap user</td></tr></tbody></table>

#### **Sample request body** <a href="#top" id="top"></a>

```json
{
    "ticker": "btc",
    "address": "0xdac17f958d2ee523a2206206994597c13d831ec7"
}
```

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the updated order.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Wed, 27 Jul 2023 15:54:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
    "success": false,
    "data": "Invalid Wallet Address"
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

