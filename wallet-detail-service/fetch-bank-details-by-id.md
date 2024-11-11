# Fetch Wallet Details by Id\*

### GET /v1/walletDetails/:id <a href="#top" id="top"></a>

Allows a User to get Wallet details by Id on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to fetch a wallet by Id.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/walletDetails/:id
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

## Request Params <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="218">Key</th><th width="129">Value</th><th>Description</th></tr></thead><tbody><tr><td>Id</td><td>&#x3C;Id></td><td>The unique ID for a specific wallet detail.</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the new wallet.

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
        "chainId": "1",
        "userId": "63d4f7a03a678d014c3c4996",
        "address": "0x483293A1Dc64A7589C994e633a03e66AE52DD130",
        "name": "Zap Africa",
        "createdAt": "2023-01-28T10:23:29.259Z",
        "updatedAt": "2023-01-28T10:23:29.259Z",
        "id": "63d4f7a13a678d014c3c499f"
    }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name          | Type                  | Description                                                           |
| ------------- | --------------------- | --------------------------------------------------------------------- |
| WalletDetails | Wallet Details Object | Contains information about the User's wallet details on ZAP platform. |



The properties included in the **WalletDetails** object are listed below.

<table><thead><tr><th width="190.33333333333331">Property</th><th width="333">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>String</td><td>The unique ID for a specific wallet detail. Used in response message.</td></tr><tr><td>chainId</td><td>String</td><td>The ID for a specific chain.</td></tr><tr><td>userId</td><td>String</td><td>The unique ID for a specific user.</td></tr><tr><td>name</td><td>String</td><td>The name of the wallet.</td></tr><tr><td>address</td><td>String</td><td>The public address of the wallet</td></tr><tr><td>isDeleted</td><td>Boolean</td><td>A flag indicating whether the wallet has been deleted.</td></tr><tr><td>deletedAt</td><td>dateTime</td><td>The timestamp when the wallet was marked as deleted.</td></tr><tr><td>createdAt</td><td>dateTime</td><td>This property displays when the wallet detail was created. Used only in response messages.</td></tr><tr><td>updatedAt</td><td>dateTime</td><td>This property displays when the wallet detail was last updated. Used only in response messages.</td></tr></tbody></table>

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                   |
| ---- | --------------------------------------- |
| 404  | The resource could not be found.        |
| 500  | An error occured processing the request |
