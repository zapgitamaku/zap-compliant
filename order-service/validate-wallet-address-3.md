---
description: Endpoint to get supported tokens on ZAP server
---

# Get Supported Chains

### GET /v1/orders/chains <a href="#top" id="top"></a>

Gets all supported chains on zap server

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to validate a zap user receiving wallet address on the platform.

#### **Sample request** URL <a href="#top" id="top"></a>

<pre><code><strong>v1/orders/chains
</strong></code></pre>

#### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header       | Description      |
| ------------ | ---------------- |
| Content-type | application/json |

#### Response <a href="#top" id="top"></a>

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
    "success": true,
    "data": [
        {
            "name": "Ethereum",
            "icon": "https://res.cloudinary.com/dukdbbrbc/image/upload/v1684235469/image/ether.svg",
            "chainId": "1"
        },
        {
            "name": "Optimism",
            "icon": "https://res.cloudinary.com/dukdbbrbc/image/upload/v1712753080/icons/1712753081087.svg",
            "chainId": "10"
        },
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th>Name</th><th>Type</th><th width="178">Description</th><th></th></tr></thead><tbody><tr><td>Success</td><td>Boolean</td><td>Returns true or false for a description</td><td>true</td></tr><tr><td>Data Array</td><td>Array </td><td>Array of chains supported by ZAP</td><td></td></tr></tbody></table>

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |
