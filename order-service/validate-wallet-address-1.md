# Get Unsigned Transaction Object

### GET /v1/orders/:id/unsignedTx <a href="#top" id="top"></a>

Creates an unsigned transaction on the backend using the blockchain manager.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to validate a zap user receiving wallet address on the platform.

#### **Sample request** URL <a href="#top" id="top"></a>

```
/v1/orders/{orderId}/unsignedTx
```

#### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header       | Description      |
| ------------ | ---------------- |
| Content-type | application/json |

## Request Query <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="125">Key</th><th>Value</th><th>Description</th></tr></thead><tbody><tr><td>senderAddress</td><td>String</td><td>The address sending the transaction.</td></tr></tbody></table>

#### **Sample request body** <a href="#top" id="top"></a>

```json
{
    "senderAddress": "0x5a52e96bacdabb82fd05763e25335261b270efcb",
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
    "success": true,
    "data": {
        "from": "0x5a52e96bacdabb82fd05763e25335261b270efcb",
        "to": "0x5A8D28b2De9cabE0FA1Ad9f307F04E2F6B9124BA",
        "value": {
            "type": "BigNumber",
            "hex": "0x1c6bf526340000"
        },
        "gasLimit": {
            "type": "BigNumber",
            "hex": "0xa2a4f9e0419c"
        },
        "maxFeePerGas": "16.69742769",
        "maxPriorityFeePerGas": "8.348713845",
        "data": "0x"
    } //varies depending on the chain involved
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="253">Name</th><th>Type</th><th width="178">Description</th><th></th></tr></thead><tbody><tr><td>Success</td><td>Boolean</td><td>Returns true or false for a description</td><td>true</td></tr><tr><td>Data Object</td><td>Object</td><td>Contains information about the transaction object.</td><td></td></tr></tbody></table>

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |
